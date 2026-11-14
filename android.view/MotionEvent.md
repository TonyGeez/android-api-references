# MotionEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MotionEvent

Kotlin| [Java](https://developer.android.com/reference/android/view/MotionEvent "View this page in Java") 

```
class MotionEvent : InputEvent, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.view.InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent) ||
| | ↳ | [android.view.MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#) |

Object used to report movement (mouse, pen, finger, trackball) events. Motion events may hold either absolute or relative movements and other data, depending on the type of device.

### Overview

<br />

Motion events describe movements in terms of an action code and a set of axis values. The action code specifies the state change that occurred such as a pointer going down or up. The axis values describe the position and other movement properties.

For example, when the user first touches the screen, the system delivers a touch event to the appropriate [View](https://developer.android.com/reference/kotlin/android/view/View) with the action code [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) and a set of axis values that include the X and Y coordinates of the touch and information about the pressure, size and orientation of the contact area.

Some devices can report multiple movement traces at the same time. Multi-touch screens emit one movement trace for each finger. The individual fingers or other objects that generate movement traces are referred to as*pointers*. Motion events contain information about all of the pointers that are currently active even if some of them have not moved since the last event was delivered.

The number of pointers only ever changes by one as individual pointers go up and down, except when the gesture is canceled.

Each pointer has a unique id that is assigned when it first goes down (indicated by [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) or [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int)). A pointer id remains valid until the pointer eventually goes up (indicated by [ACTION_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int) or [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int)) or when the gesture is canceled (indicated by [ACTION_CANCEL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int)).

The MotionEvent class provides many methods to query the position and other properties of pointers, such as [getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int)), [getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int)), #getAxisValue, [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int)), [getToolType(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolType(kotlin.Int)), and many others. Most of these methods accept the pointer index as a parameter rather than the pointer id. The pointer index of each pointer in the event ranges from 0 to one less than the value returned by [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount()).

The order in which individual pointers appear within a motion event is undefined. Thus the pointer index of a pointer can change from one event to the next but the pointer id of a pointer is guaranteed to remain constant as long as the pointer remains active. Use the [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int))method to obtain the pointer id of a pointer to track it across all subsequent motion events in a gesture. Then for successive motion events, use the [findPointerIndex(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#findPointerIndex(kotlin.Int))method to obtain the pointer index for a given pointer id in that motion event.

Mouse and stylus buttons can be retrieved using [getButtonState()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState()). It is a good idea to check the button state while handling [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) as part of a touch event. The application may choose to perform some different action if the touch event starts due to a secondary button click, such as presenting a context menu.

### Batching

For efficiency, motion events with [ACTION_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int) may batch together multiple movement samples within a single object. The most current pointer coordinates are available using [getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int))and [getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int)). Earlier coordinates within the batch are accessed using [getHistoricalX(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalX(kotlin.Int,%20kotlin.Int))and [getHistoricalY(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalY(kotlin.Int,%20kotlin.Int)). The coordinates are "historical" only insofar as they are older than the current coordinates in the batch; however, they are still distinct from any other coordinates reported in prior motion events. To process all coordinates in the batch in time order, first consume the historical coordinates then consume the current coordinates.

Example: Consuming all samples for all pointers in a motion event in time order.

<br />

```kotlin
<code>
  void printSamples(MotionEvent ev) {
      final int historySize = ev.getHistorySize();
      final int pointerCount = ev.getPointerCount();
      for (int h = 0; h &lt; historySize; h++) {
          System.out.printf("At time %d:", ev.getHistoricalEventTime(h));
          for (int p = 0; p &lt; pointerCount; p++) {
              System.out.printf("  pointer %d: (%f,%f)",
                  ev.getPointerId(p), ev.getHistoricalX(p, h), ev.getHistoricalY(p, h));
          }
      }
      System.out.printf("At time %d:", ev.getEventTime());
      for (int p = 0; p &lt; pointerCount; p++) {
          System.out.printf("  pointer %d: (%f,%f)",
              ev.getPointerId(p), ev.getX(p), ev.getY(p));
      }
  }
  </code>
```

<br />

Developers should keep in mind that it is especially important to consume all samples in a batched event when processing relative values that report changes since the last event or sample. Examples of such relative axes include [AXIS_RELATIVE_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RELATIVE_X:kotlin.Int), [AXIS_RELATIVE_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RELATIVE_Y:kotlin.Int), and many of the axes prefixed with`AXIS_GESTURE_`. In these cases, developers should first consume all historical values using [getHistoricalAxisValue(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int))and then consume the current values using [getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int))like in the example above, as these relative values are not accumulated in a batched event.

### Device Types

The interpretation of the contents of a MotionEvent varies significantly depending on the source class of the device.

On pointing devices with source class [InputDevice.SOURCE_CLASS_POINTER](https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_POINTER:kotlin.Int) such as touch screens, the pointer coordinates specify absolute positions such as view X/Y coordinates. Each complete gesture is represented by a sequence of motion events with actions that describe pointer state transitions and movements. A gesture starts with a motion event with [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) that provides the location of the first pointer down. As each additional pointer that goes down or up, the framework will generate a motion event with [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int) or [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int) accordingly. Pointer movements are described by motion events with [ACTION_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int). Finally, a gesture end either when the final pointer goes up as represented by a motion event with [ACTION_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int) or when gesture is canceled with [ACTION_CANCEL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int).

Some pointing devices such as mice may support vertical and/or horizontal scrolling. A scroll event is reported as a generic motion event with [ACTION_SCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_SCROLL:kotlin.Int) that includes the relative scroll offset in the [AXIS_VSCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_VSCROLL:kotlin.Int) and [AXIS_HSCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_HSCROLL:kotlin.Int) axes. See [getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int))for information about retrieving these additional axes.

On trackball devices with source class [InputDevice.SOURCE_CLASS_TRACKBALL](https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_TRACKBALL:kotlin.Int), the pointer coordinates specify relative movements as X/Y deltas. A trackball gesture consists of a sequence of movements described by motion events with [ACTION_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int) interspersed with occasional [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) or [ACTION_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int) motion events when the trackball button is pressed or released.

On joystick devices with source class [InputDevice.SOURCE_CLASS_JOYSTICK](https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_JOYSTICK:kotlin.Int), the pointer coordinates specify the absolute position of the joystick axes. The joystick axis values are normalized to a range of -1.0 to 1.0 where 0.0 corresponds to the center position. More information about the set of available axes and the range of motion can be obtained using android.view.InputDevice#getMotionRange. Some common joystick axes are [AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int), [AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int), [AXIS_HAT_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_HAT_X:kotlin.Int), [AXIS_HAT_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_HAT_Y:kotlin.Int), [AXIS_Z](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Z:kotlin.Int) and [AXIS_RZ](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RZ:kotlin.Int).

Refer to [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) for more information about how different kinds of input devices and sources represent pointer coordinates.

### Consistency Guarantees

Motion events are always delivered to views as a consistent stream of events. What constitutes a consistent stream varies depending on the type of device. For touch events, consistency implies that pointers go down one at a time, move around as a group and then go up one at a time or are canceled.

While the framework tries to deliver consistent streams of motion events to views, it cannot guarantee it. Some events may be dropped or modified by containing views in the application before they are delivered thereby making the stream of events inconsistent. Views should always be prepared to handle [ACTION_CANCEL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int) and should tolerate anomalous situations such as receiving a new [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) without first having received an [ACTION_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int) for the prior gesture.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) Transfer object for pointer coordinates. |
| | [PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties) Transfer object for pointer properties. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_BUTTON_PRESS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_BUTTON_PRESS:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A button has been pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_BUTTON_RELEASE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_BUTTON_RELEASE:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A button has been released. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_CANCEL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): The current gesture has been aborted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A pressed gesture has started, the motion contains the initial starting location. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_HOVER_ENTER](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_ENTER:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): The pointer is not down but has entered the boundaries of a window or view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_HOVER_EXIT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_EXIT:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): The pointer is not down but has exited the boundaries of a window or view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_HOVER_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_MOVE:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A change happened but the pointer is not down (unlike [ACTION_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MASK:kotlin.Int) Bit mask of the parts of the action code that are the action itself. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A change has happened during a press gesture (between [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) and [ACTION_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_OUTSIDE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_OUTSIDE:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A movement has happened outside of the normal bounds of the UI element. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_1_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_1_DOWN:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_1_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_1_UP:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_2_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_2_DOWN:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_2_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_2_UP:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_3_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_3_DOWN:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_3_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_3_UP:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A non-primary pointer has gone down. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_ID_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_ID_MASK:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_ID_SHIFT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_ID_SHIFT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) Bits in the action code that represent a pointer index, used with [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int) and [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_INDEX_SHIFT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_SHIFT:kotlin.Int) Bit shift for the action bits holding the pointer index as defined by [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A non-primary pointer has gone up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_SCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_SCROLL:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): The motion event contains relative vertical and/or horizontal scroll offsets. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACTION_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int) Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A pressed gesture has finished, the motion contains the final release location as well as any intermediate points since the last down or move event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_BRAKE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_BRAKE:kotlin.Int) Axis constant: Brake axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_DISTANCE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_DISTANCE:kotlin.Int) Axis constant: Distance axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GAS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GAS:kotlin.Int) Axis constant: Gas axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_1](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_1:kotlin.Int) Axis constant: Generic 1 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_10](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_10:kotlin.Int) Axis constant: Generic 10 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_11](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_11:kotlin.Int) Axis constant: Generic 11 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_12](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_12:kotlin.Int) Axis constant: Generic 12 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_13](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_13:kotlin.Int) Axis constant: Generic 13 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_14](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_14:kotlin.Int) Axis constant: Generic 14 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_15](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_15:kotlin.Int) Axis constant: Generic 15 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_16](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_16:kotlin.Int) Axis constant: Generic 16 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_2](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_2:kotlin.Int) Axis constant: Generic 2 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_3](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_3:kotlin.Int) Axis constant: Generic 3 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_4](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_4:kotlin.Int) Axis constant: Generic 4 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_5](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_5:kotlin.Int) Axis constant: Generic 5 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_6](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_6:kotlin.Int) Axis constant: Generic 6 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_7](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_7:kotlin.Int) Axis constant: Generic 7 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_8](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_8:kotlin.Int) Axis constant: Generic 8 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GENERIC_9](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GENERIC_9:kotlin.Int) Axis constant: Generic 9 axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GESTURE_PINCH_SCALE_FACTOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GESTURE_PINCH_SCALE_FACTOR:kotlin.Int) Axis constant: pinch scale factor of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GESTURE_SCROLL_X_DISTANCE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GESTURE_SCROLL_X_DISTANCE:kotlin.Int) Axis constant: X scroll distance axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GESTURE_SCROLL_Y_DISTANCE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GESTURE_SCROLL_Y_DISTANCE:kotlin.Int) Axis constant: Y scroll distance axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GESTURE_X_OFFSET](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GESTURE_X_OFFSET:kotlin.Int) Axis constant: X gesture offset axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_GESTURE_Y_OFFSET](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GESTURE_Y_OFFSET:kotlin.Int) Axis constant: Y gesture offset axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_HAT_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_HAT_X:kotlin.Int) Axis constant: Hat X axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_HAT_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_HAT_Y:kotlin.Int) Axis constant: Hat Y axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_HSCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_HSCROLL:kotlin.Int) Axis constant: Horizontal Scroll axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_LTRIGGER](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_LTRIGGER:kotlin.Int) Axis constant: Left Trigger axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_ORIENTATION](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_ORIENTATION:kotlin.Int) Axis constant: Orientation axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_PRESSURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_PRESSURE:kotlin.Int) Axis constant: Pressure axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_RELATIVE_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RELATIVE_X:kotlin.Int) Axis constant: The movement of x position of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_RELATIVE_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RELATIVE_Y:kotlin.Int) Axis constant: The movement of y position of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_RTRIGGER](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RTRIGGER:kotlin.Int) Axis constant: Right Trigger axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_RUDDER](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RUDDER:kotlin.Int) Axis constant: Rudder axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_RX](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RX:kotlin.Int) Axis constant: X Rotation axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_RY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RY:kotlin.Int) Axis constant: Y Rotation axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_RZ](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RZ:kotlin.Int) Axis constant: Z Rotation axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_SCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_SCROLL:kotlin.Int) Axis constant: Generic scroll axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_SIZE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_SIZE:kotlin.Int) Axis constant: Size axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_THROTTLE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_THROTTLE:kotlin.Int) Axis constant: Throttle axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_TILT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TILT:kotlin.Int) Axis constant: Tilt axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_TOOL_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int) Axis constant: ToolMajor axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_TOOL_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MINOR:kotlin.Int) Axis constant: ToolMinor axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_TOUCH_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int) Axis constant: TouchMajor axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_TOUCH_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MINOR:kotlin.Int) Axis constant: TouchMinor axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_VSCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_VSCROLL:kotlin.Int) Axis constant: Vertical Scroll axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_WHEEL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_WHEEL:kotlin.Int) Axis constant: Wheel axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int) Axis constant: X axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) Axis constant: Y axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_Z](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Z:kotlin.Int) Axis constant: Z axis of a motion event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_BACK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_BACK:kotlin.Int) Button constant: Back button pressed (mouse back button). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_FORWARD](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_FORWARD:kotlin.Int) Button constant: Forward button pressed (mouse forward button). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_PRIMARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_PRIMARY:kotlin.Int) Button constant: Primary button (left mouse button). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_SECONDARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_SECONDARY:kotlin.Int) Button constant: Secondary button (right mouse button). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_STYLUS_PRIMARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_STYLUS_PRIMARY:kotlin.Int) Button constant: Primary stylus button pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_STYLUS_SECONDARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_STYLUS_SECONDARY:kotlin.Int) Button constant: Secondary stylus button pressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_TERTIARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_TERTIARY:kotlin.Int) Button constant: Tertiary button (middle mouse button). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLASSIFICATION_AMBIGUOUS_GESTURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_AMBIGUOUS_GESTURE:kotlin.Int) Classification constant: Ambiguous gesture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLASSIFICATION_DEEP_PRESS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_DEEP_PRESS:kotlin.Int) Classification constant: Deep press. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLASSIFICATION_NONE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_NONE:kotlin.Int) Classification constant: None. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLASSIFICATION_PINCH](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_PINCH:kotlin.Int) Classification constant: touchpad pinch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLASSIFICATION_TWO_FINGER_SWIPE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_TWO_FINGER_SWIPE:kotlin.Int) Classification constant: touchpad scroll. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDGE_BOTTOM](https://developer.android.com/reference/kotlin/android/view/MotionEvent#EDGE_BOTTOM:kotlin.Int) Flag indicating the motion event intersected the bottom edge of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDGE_LEFT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#EDGE_LEFT:kotlin.Int) Flag indicating the motion event intersected the left edge of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDGE_RIGHT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#EDGE_RIGHT:kotlin.Int) Flag indicating the motion event intersected the right edge of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDGE_TOP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#EDGE_TOP:kotlin.Int) Flag indicating the motion event intersected the top edge of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CANCELED](https://developer.android.com/reference/kotlin/android/view/MotionEvent#FLAG_CANCELED:kotlin.Int) This flag is only set for events with [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int) and [ACTION_CANCEL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_WINDOW_IS_OBSCURED](https://developer.android.com/reference/kotlin/android/view/MotionEvent#FLAG_WINDOW_IS_OBSCURED:kotlin.Int) This flag indicates that the window that received this motion event is partly or wholly obscured by another visible window above it and the event directly passed through the obscured area. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_WINDOW_IS_PARTIALLY_OBSCURED](https://developer.android.com/reference/kotlin/android/view/MotionEvent#FLAG_WINDOW_IS_PARTIALLY_OBSCURED:kotlin.Int) This flag indicates that the window that received this motion event is partly or wholly obscured by another visible window above it and the event did not directly pass through the obscured area. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_POINTER_ID](https://developer.android.com/reference/kotlin/android/view/MotionEvent#INVALID_POINTER_ID:kotlin.Int) An invalid pointer id. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOOL_TYPE_ERASER](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_ERASER:kotlin.Int) Tool type constant: The tool is an eraser or a stylus being used in an inverted posture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOOL_TYPE_FINGER](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_FINGER:kotlin.Int) Tool type constant: The tool is a finger. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOOL_TYPE_MOUSE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_MOUSE:kotlin.Int) Tool type constant: The tool is a mouse. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOOL_TYPE_STYLUS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_STYLUS:kotlin.Int) Tool type constant: The tool is a stylus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOOL_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_UNKNOWN:kotlin.Int) Tool type constant: Unknown tool type. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [actionToString](https://developer.android.com/reference/kotlin/android/view/MotionEvent#actionToString(kotlin.Int))`(`action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string that represents the symbolic name of the specified unmasked action such as "ACTION_DOWN", "ACTION_POINTER_DOWN(3)" or an equivalent numeric constant such as "35" if unknown. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addBatch](https://developer.android.com/reference/kotlin/android/view/MotionEvent#addBatch(kotlin.Long,%20kotlin.Array,%20kotlin.Int))`(`eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `pointerCoords:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!>!`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Add a new movement to the batch of movements in this event. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addBatch](https://developer.android.com/reference/kotlin/android/view/MotionEvent#addBatch(kotlin.Long,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int))`(`eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pressure:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `size:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Add a new movement to the batch of movements in this event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [axisFromString](https://developer.android.com/reference/kotlin/android/view/MotionEvent#axisFromString(kotlin.String))`(`symbolicName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets an axis by its symbolic name such as "AXIS_X" or an equivalent numeric constant such as "42". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [axisToString](https://developer.android.com/reference/kotlin/android/view/MotionEvent#axisToString(kotlin.Int))`(`axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string that represents the symbolic name of the specified axis such as "AXIS_X" or an equivalent numeric constant such as "42" if unknown. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findPointerIndex](https://developer.android.com/reference/kotlin/android/view/MotionEvent#findPointerIndex(kotlin.Int))`(`pointerId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Given a pointer identifier, find the index of its data in the event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAction](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAction())`()` Return the kind of action being performed. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActionButton](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionButton())`()` Gets which button has been modified during a press or release action. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActionIndex](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionIndex())`()` For [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int) or [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int) as returned by [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()), this returns the associated pointer index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked())`()` Return the masked action being performed, without pointer index information. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAxisValue](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int))`(`axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAxisValue](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))`(`axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested axis for the given pointer*index* (use [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int))to find the pointer identifier for this index). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getButtonState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState())`()` Gets the state of all buttons that are pressed such as a mouse or stylus button. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getClassification](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getClassification())`()` Returns the classification for the current gesture. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceId](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getDeviceId())`()` Gets the id for the device that this event came from. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDownTime](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getDownTime())`()` Returns the time (in ms) when the user originally pressed down to start a stream of position events. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEdgeFlags](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getEdgeFlags())`()` Returns a bitfield indicating which edges, if any, were touched by this MotionEvent. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEventTime](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getEventTime())`()` Retrieve the time this event occurred, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEventTimeNanos](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getEventTimeNanos())`()` Retrieve the time this event occurred, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base but with nanosecond precision. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getFlags())`()` Gets the motion event flags. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalAxisValue](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int))`(`axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalAxisValue(int,int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalAxisValue](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the historical value of the requested axis, as per [getAxisValue(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int)), occurred between this event and the previous event for the given pointer. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getHistoricalEventTime](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalEventTime(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the time that a historical movement occurred between this event and the previous event, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getHistoricalEventTimeNanos](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalEventTimeNanos(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the time that a historical movement occurred between this event and the previous event, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base but with nanosecond (instead of millisecond) precision. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalOrientation](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalOrientation(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalOrientation(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalOrientation(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalOrientation](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalOrientation(kotlin.Int,%20kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a historical orientation coordinate, as per [getOrientation(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getOrientation(kotlin.Int)), that occurred between this event and the previous event for the given pointer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getHistoricalPointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalPointerCoords(kotlin.Int,%20kotlin.Int,%20android.view.MotionEvent.PointerCoords))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outPointerCoords:` ` [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!`)` Populates a [PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) object with historical pointer coordinate data, as per [getPointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCoords(kotlin.Int,%20android.view.MotionEvent.PointerCoords)), that occurred between this event and the previous event for the given pointer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalPressure](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalPressure(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalPressure(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalPressure(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalPressure](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalPressure(kotlin.Int,%20kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a historical pressure coordinate, as per [getPressure(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure(kotlin.Int)), that occurred between this event and the previous event for the given pointer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalSize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalSize(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalSize(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalSize(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalSize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalSize(kotlin.Int,%20kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a historical size coordinate, as per [getSize(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize(kotlin.Int)), that occurred between this event and the previous event for the given pointer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalToolMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMajor(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalToolMajor(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMajor(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalToolMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMajor(kotlin.Int,%20kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a historical tool major axis coordinate, as per [getToolMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMajor(kotlin.Int)), that occurred between this event and the previous event for the given pointer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalToolMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMinor(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalToolMinor(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMinor(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalToolMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMinor(kotlin.Int,%20kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a historical tool minor axis coordinate, as per [getToolMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMinor(kotlin.Int)), that occurred between this event and the previous event for the given pointer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalTouchMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMajor(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalTouchMajor(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMajor(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalTouchMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMajor(kotlin.Int,%20kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a historical touch major axis coordinate, as per [getTouchMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMajor(kotlin.Int)), that occurred between this event and the previous event for the given pointer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalTouchMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMinor(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalTouchMinor(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMinor(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalTouchMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMinor(kotlin.Int,%20kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a historical touch minor axis coordinate, as per [getTouchMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMinor(kotlin.Int)), that occurred between this event and the previous event for the given pointer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalX](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalX(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalX(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalX(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalX](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalX(kotlin.Int,%20kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a historical X coordinate, as per [getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int)), that occurred between this event and the previous event for the given pointer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalY(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [getHistoricalY(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalY(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHistoricalY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalY(kotlin.Int,%20kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a historical Y coordinate, as per [getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int)), that occurred between this event and the previous event for the given pointer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())`()` Returns the number of historical points in this event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getMetaState())`()` Returns the state of any meta / modifier keys that were in effect when the event was generated. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getOrientation](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getOrientation())`()` [getOrientation(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getOrientation(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getOrientation](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getOrientation(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of [AXIS_ORIENTATION](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_ORIENTATION:kotlin.Int) for the given pointer*index*. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getPointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCoords(kotlin.Int,%20android.view.MotionEvent.PointerCoords))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outPointerCoords:` ` [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!`)` Populates a [PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) object with pointer coordinate data for the specified pointer index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPointerCount](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())`()` The number of pointers of data contained in this event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPointerId](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the pointer identifier associated with a particular pointer data index in this event. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getPointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerProperties(kotlin.Int,%20android.view.MotionEvent.PointerProperties))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outPointerProperties:` ` [MotionEvent.PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties)!`)` Populates a [PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties) object with pointer properties for the specified pointer index. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPressure](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure())`()` [getPressure(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPressure](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of [AXIS_PRESSURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_PRESSURE:kotlin.Int) for the given pointer*index*. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRawX](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getRawX())`()` Equivalent to [getRawX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getRawX(kotlin.Int))for pointer index 0 (regardless of the pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRawX](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getRawX(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the X coordinate of the pointer referenced by`pointerIndex`for this motion event. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRawY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getRawY())`()` Equivalent to [getRawY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getRawY(kotlin.Int))for pointer index 0 (regardless of the pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRawY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getRawY(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the Y coordinate of the pointer referenced by`pointerIndex`for this motion event. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize())`()` [getSize(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of [AXIS_SIZE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_SIZE:kotlin.Int) for the given pointer*index*. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSource](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSource())`()` Gets the source of the event. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getToolMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMajor())`()` [getToolMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMajor(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getToolMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMajor(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of [AXIS_TOOL_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int) for the given pointer*index*. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getToolMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMinor())`()` [getToolMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMinor(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getToolMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMinor(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of [AXIS_TOOL_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MINOR:kotlin.Int) for the given pointer*index*. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getToolType](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolType(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the tool type of a pointer for the given pointer index. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getTouchMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMajor())`()` [getTouchMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMajor(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getTouchMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMajor(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of [AXIS_TOUCH_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int) for the given pointer*index*. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getTouchMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMinor())`()` [getTouchMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMinor(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getTouchMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMinor(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of [AXIS_TOUCH_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MINOR:kotlin.Int) for the given pointer*index*. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getX](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX())`()` Equivalent to [getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int))for pointer index 0 (regardless of the pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getX](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the X coordinate of the pointer referenced by`pointerIndex`for this motion event. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getXPrecision](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getXPrecision())`()` Return the precision of the X coordinates being reported. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY())`()` Equivalent to [getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int))for pointer index 0 (regardless of the pointer identifier). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int))`(`pointerIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the Y coordinate of the pointer referenced by`pointerIndex`for this motion event. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getYPrecision](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getYPrecision())`()` Return the precision of the Y coordinates being reported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isButtonPressed](https://developer.android.com/reference/kotlin/android/view/MotionEvent#isButtonPressed(kotlin.Int))`(`button:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if a mouse or stylus button (or combination of buttons) is pressed. |
| static [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)! | [obtain](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(android.view.MotionEvent))`(`other:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)!`)` Create a new MotionEvent, copying from an existing one. |
| static [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)! | [obtain](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int))`(`downTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pressure:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `size:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `edgeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new MotionEvent, filling in all of the basic values that define the motion. |
| static [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)! | [obtain](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int))`(`downTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new MotionEvent, filling in a subset of the basic motion values. |
| static [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)! | [obtain](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array,%20kotlin.Array,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`downTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointerCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointerProperties:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MotionEvent.PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties)!>!`, `pointerCoords:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!>!`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buttonState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `edgeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new MotionEvent, filling in all of the basic values that define the motion. |
| static [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)? | [obtain](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array,%20kotlin.Array,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`downTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointerCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointerProperties:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MotionEvent.PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties)!>`, `pointerCoords:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!>`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buttonState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `edgeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `classification:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new MotionEvent, filling in all of the basic values that define the motion. |
| static [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)! | [obtain](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int))`(`downTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointerCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pressure:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `size:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `edgeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new MotionEvent, filling in all of the basic values that define the motion. |
| static [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)! | [obtain](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Array,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`downTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointerCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointerIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `pointerCoords:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!>!`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yPrecision:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `edgeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new MotionEvent, filling in all of the basic values that define the motion. |
| static [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)! | [obtainNoHistory](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtainNoHistory(android.view.MotionEvent))`(`other:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)!`)` Create a new MotionEvent, copying from an existing one, but not including any historical point information. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [offsetLocation](https://developer.android.com/reference/kotlin/android/view/MotionEvent#offsetLocation(kotlin.Float,%20kotlin.Float))`(`deltaX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `deltaY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Adjust this event's location. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](https://developer.android.com/reference/kotlin/android/view/MotionEvent#recycle())`()` Recycle the MotionEvent, to be re-used by a later caller. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAction](https://developer.android.com/reference/kotlin/android/view/MotionEvent#setAction(kotlin.Int))`(`action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this event's action. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEdgeFlags](https://developer.android.com/reference/kotlin/android/view/MotionEvent#setEdgeFlags(kotlin.Int))`(`flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bitfield indicating which edges, if any, were touched by this MotionEvent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocation](https://developer.android.com/reference/kotlin/android/view/MotionEvent#setLocation(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set this event's location. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSource](https://developer.android.com/reference/kotlin/android/view/MotionEvent#setSource(kotlin.Int))`(`source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/MotionEvent#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transform](https://developer.android.com/reference/kotlin/android/view/MotionEvent#transform(android.graphics.Matrix))`(`matrix:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)!`)` Applies a transformation matrix to all of the points in the event. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/MotionEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#finalize())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent) |-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/InputEvent#describeContents())`()` <br /> | | [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice)! | [getDevice](https://developer.android.com/reference/kotlin/android/view/InputEvent#getDevice())`()` <br /> Gets the device that this event came from. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFromSource](https://developer.android.com/reference/kotlin/android/view/InputEvent#isFromSource(kotlin.Int))`(`source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Determines whether the event is from the given source. <br /> | ||
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Flatten this object in to a Parcel. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ACTION_BUTTON_PRESS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_BUTTON_PRESS: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A button has been pressed.

Use [getActionButton()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionButton())to get which button was pressed.

This action is not a touch event so it is delivered to [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onGenericMotionEvent(android.view.MotionEvent))rather than [View.onTouchEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)). 

 Value: 11

### ACTION_BUTTON_RELEASE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_BUTTON_RELEASE: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A button has been released.

Use [getActionButton()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionButton())to get which button was released.

This action is not a touch event so it is delivered to [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onGenericMotionEvent(android.view.MotionEvent))rather than [View.onTouchEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)). 

 Value: 12

### ACTION_CANCEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CANCEL: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): The current gesture has been aborted. You will not receive any more points in it. You should treat this as an up event, but not perform any action that you normally would. 

 Value: 3

### ACTION_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_DOWN: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A pressed gesture has started, the motion contains the initial starting location.

This is also a good time to check the button state to distinguish secondary and tertiary button clicks and handle them appropriately. Use [getButtonState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState())to retrieve the button state. 

 Value: 0

### ACTION_HOVER_ENTER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_HOVER_ENTER: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): The pointer is not down but has entered the boundaries of a window or view.

This action is always delivered to the window or view under the pointer.

This action is not a touch event so it is delivered to [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onGenericMotionEvent(android.view.MotionEvent))rather than [View.onTouchEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)). 

 Value: 9

### ACTION_HOVER_EXIT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_HOVER_EXIT: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): The pointer is not down but has exited the boundaries of a window or view.

This action is always delivered to the window or view that was previously under the pointer.

This action is not a touch event so it is delivered to [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onGenericMotionEvent(android.view.MotionEvent))rather than [View.onTouchEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)). 

 Value: 10

### ACTION_HOVER_MOVE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_HOVER_MOVE: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A change happened but the pointer is not down (unlike [ACTION_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int)). The motion contains the most recent point, as well as any intermediate points since the last hover move event.

This action is always delivered to the window or view under the pointer.

This action is not a touch event so it is delivered to [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onGenericMotionEvent(android.view.MotionEvent))rather than [View.onTouchEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)). 

 Value: 7

### ACTION_MASK

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_MASK: Int
```

Bit mask of the parts of the action code that are the action itself. 

 Value: 255

### ACTION_MOVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_MOVE: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A change has happened during a press gesture (between [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) and [ACTION_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_UP:kotlin.Int)). The motion contains the most recent point, as well as any intermediate points since the last down or move event. 

 Value: 2

### ACTION_OUTSIDE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_OUTSIDE: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A movement has happened outside of the normal bounds of the UI element. This does not provide a full gesture, but only the initial location of the movement/touch.

Note: Because the location of any event will be outside the bounds of the view hierarchy, it will not get dispatched to any children of a ViewGroup by default. Therefore, movements with ACTION_OUTSIDE should be handled in either the root [View](https://developer.android.com/reference/kotlin/android/view/View) or in the appropriate [Window.Callback](https://developer.android.com/reference/kotlin/android/view/Window.Callback)(e.g. [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) or [android.app.Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog.html#)). 

 Value: 4

### ACTION_POINTER_1_DOWN

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_1_DOWN: Int
```

**Deprecated:** *Use [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) to retrieve the data index associated with [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int).* 

 Value: 5

### ACTION_POINTER_1_UP

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_1_UP: Int
```

**Deprecated:** *Use [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) to retrieve the data index associated with [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int).* 

 Value: 6

### ACTION_POINTER_2_DOWN

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_2_DOWN: Int
```

**Deprecated:** *Use [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) to retrieve the data index associated with [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int).* 

 Value: 261

### ACTION_POINTER_2_UP

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_2_UP: Int
```

**Deprecated:** *Use [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) to retrieve the data index associated with [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int).* 

 Value: 262

### ACTION_POINTER_3_DOWN

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_3_DOWN: Int
```

**Deprecated:** *Use [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) to retrieve the data index associated with [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int).* 

 Value: 517

### ACTION_POINTER_3_UP

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_3_UP: Int
```

**Deprecated:** *Use [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) to retrieve the data index associated with [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int).* 

 Value: 518

### ACTION_POINTER_DOWN

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_DOWN: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A non-primary pointer has gone down.

Use [getActionIndex](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionIndex())to retrieve the index of the pointer that changed.

The index is encoded in the [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) bits of the unmasked action returned by [getAction](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAction()). 

 Value: 5

### ACTION_POINTER_ID_MASK

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_ID_MASK: Int
```

**Deprecated:** *Renamed to [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) to match the actual data contained in these bits.* 

 Value: 65280

### ACTION_POINTER_ID_SHIFT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_ID_SHIFT: Int
```

**Deprecated:** *Renamed to [ACTION_POINTER_INDEX_SHIFT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_SHIFT:kotlin.Int) to match the actual data contained in these bits.* 

 Value: 8

### ACTION_POINTER_INDEX_MASK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_INDEX_MASK: Int
```

Bits in the action code that represent a pointer index, used with [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int) and [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int). Shifting down by [ACTION_POINTER_INDEX_SHIFT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_SHIFT:kotlin.Int) provides the actual pointer index where the data for the pointer going up or down can be found; you can get its identifier with [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int))and the actual data with [getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int))etc. 

 Value: 65280

**See Also**

- [#getActionIndex](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionIndex()) 

### ACTION_POINTER_INDEX_SHIFT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_INDEX_SHIFT: Int
```

Bit shift for the action bits holding the pointer index as defined by [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int). 

 Value: 8

**See Also**

- [#getActionIndex](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionIndex()) 

### ACTION_POINTER_UP

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_POINTER_UP: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A non-primary pointer has gone up.

Use [getActionIndex](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionIndex())to retrieve the index of the pointer that changed.

The index is encoded in the [ACTION_POINTER_INDEX_MASK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_INDEX_MASK:kotlin.Int) bits of the unmasked action returned by [getAction](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAction()). 

 Value: 6

### ACTION_SCROLL

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SCROLL: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): The motion event contains relative vertical and/or horizontal scroll offsets. Use [getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int))to retrieve the information from [AXIS_VSCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_VSCROLL:kotlin.Int) and [AXIS_HSCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_HSCROLL:kotlin.Int). The pointer may or may not be down when this event is dispatched.

This action is always delivered to the window or view under the pointer, which may not be the window or view currently touched.

This action is not a touch event so it is delivered to [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onGenericMotionEvent(android.view.MotionEvent))rather than [View.onTouchEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)). 

 Value: 8

### ACTION_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_UP: Int
```

Constant for [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()): A pressed gesture has finished, the motion contains the final release location as well as any intermediate points since the last down or move event. 

 Value: 1

### AXIS_BRAKE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_BRAKE: Int
```

Axis constant: Brake axis of a motion event.

<br />

- For a joystick, reports the absolute position of the brake control. The value is normalized to a range from 0.0 (no braking) to 1.0 (maximum braking).

<br />

 Value: 23

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_DISTANCE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_DISTANCE: Int
```

Axis constant: Distance axis of a motion event.

<br />

- For a stylus, reports the distance of the stylus from the screen. A value of 0.0 indicates direct contact and larger values indicate increasing distance from the surface.

<br />

 Value: 24

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GAS

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GAS: Int
```

Axis constant: Gas axis of a motion event.

<br />

- For a joystick, reports the absolute position of the gas (accelerator) control. The value is normalized to a range from 0.0 (no acceleration) to 1.0 (maximum acceleration).

<br />

 Value: 22

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_1

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_1: Int
```

Axis constant: Generic 1 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 32

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_10

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_10: Int
```

Axis constant: Generic 10 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 41

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_11

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_11: Int
```

Axis constant: Generic 11 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 42

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_12

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_12: Int
```

Axis constant: Generic 12 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 43

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_13

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_13: Int
```

Axis constant: Generic 13 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 44

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_14

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_14: Int
```

Axis constant: Generic 14 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 45

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_15

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_15: Int
```

Axis constant: Generic 15 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 46

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_16

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_16: Int
```

Axis constant: Generic 16 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 47

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_2

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_2: Int
```

Axis constant: Generic 2 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 33

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_3

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_3: Int
```

Axis constant: Generic 3 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 34

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_4

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_4: Int
```

Axis constant: Generic 4 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 35

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_5

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_5: Int
```

Axis constant: Generic 5 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 36

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_6

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_6: Int
```

Axis constant: Generic 6 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 37

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_7

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_7: Int
```

Axis constant: Generic 7 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 38

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_8

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_8: Int
```

Axis constant: Generic 8 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 39

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GENERIC_9

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GENERIC_9: Int
```

Axis constant: Generic 9 axis of a motion event. The interpretation of a generic axis is device-specific. 

 Value: 40

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_GESTURE_PINCH_SCALE_FACTOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GESTURE_PINCH_SCALE_FACTOR: Int
```

Axis constant: pinch scale factor of a motion event.

<br />

- For a touch pad, reports the change in distance between the fingers when the user is making a pinch gesture, as a proportion of the previous distance. For example, if the fingers were 50 units apart and are now 52 units apart, the scale factor would be 1.04.

These values are relative to the state from the last sample, not accumulated, so developers should make sure to process this axis value for all batched historical samples.

This axis is only set on the first pointer in a motion event. 

 Value: 52

### AXIS_GESTURE_SCROLL_X_DISTANCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GESTURE_SCROLL_X_DISTANCE: Int
```

Axis constant: X scroll distance axis of a motion event.

<br />

- For a touch pad, reports the distance that should be scrolled in the X axis as a result of the user's two-finger scroll gesture, in display pixels.

These values are relative to the state from the last sample, not accumulated, so developers should make sure to process this axis value for all batched historical samples.

This axis is only set on the first pointer in a motion event. 

 Value: 50

### AXIS_GESTURE_SCROLL_Y_DISTANCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GESTURE_SCROLL_Y_DISTANCE: Int
```

Axis constant: Y scroll distance axis of a motion event. The same as [AXIS_GESTURE_SCROLL_X_DISTANCE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GESTURE_SCROLL_X_DISTANCE:kotlin.Int), but for the Y axis. 

 Value: 51

### AXIS_GESTURE_X_OFFSET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GESTURE_X_OFFSET: Int
```

Axis constant: X gesture offset axis of a motion event.

<br />

- For a touch pad, reports the distance that a swipe gesture has moved in the X axis, as a proportion of the touch pad's size. For example, if a touch pad is 1000 units wide, and a swipe gesture starts at X = 500 then moves to X = 400, this axis would have a value of -0.1.

These values are relative to the state from the last sample, not accumulated, so developers should make sure to process this axis value for all batched historical samples.

This axis is only set on the first pointer in a motion event. 

 Value: 48

### AXIS_GESTURE_Y_OFFSET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_GESTURE_Y_OFFSET: Int
```

Axis constant: Y gesture offset axis of a motion event. The same as [AXIS_GESTURE_X_OFFSET](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_GESTURE_X_OFFSET:kotlin.Int), but for the Y axis. 

 Value: 49

### AXIS_HAT_X

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_HAT_X: Int
```

Axis constant: Hat X axis of a motion event.

<br />

- For a joystick, reports the absolute X position of the directional hat control. The value is normalized to a range from -1.0 (left) to 1.0 (right).

<br />

 Value: 15

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_HAT_Y

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_HAT_Y: Int
```

Axis constant: Hat Y axis of a motion event.

<br />

- For a joystick, reports the absolute Y position of the directional hat control. The value is normalized to a range from -1.0 (up) to 1.0 (down).

<br />

 Value: 16

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_HSCROLL

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_HSCROLL: Int
```

Axis constant: Horizontal Scroll axis of a motion event.

<br />

- For a mouse, reports the relative movement of the horizontal scroll wheel. The value is normalized to a range from -1.0 (left) to 1.0 (right).

<br />

This axis should be used to scroll views horizontally. 

 Value: 10

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_LTRIGGER

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_LTRIGGER: Int
```

Axis constant: Left Trigger axis of a motion event.

<br />

- For a joystick, reports the absolute position of the left trigger control. The value is normalized to a range from 0.0 (released) to 1.0 (fully pressed).

<br />

 Value: 17

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_ORIENTATION

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_ORIENTATION: Int
```

Axis constant: Orientation axis of a motion event.

<br />

- For a touch screen or touch pad, reports the orientation of the finger or tool in radians relative to the vertical plane of the device. An angle of 0 radians indicates that the major axis of contact is oriented upwards, is perfectly circular or is of unknown orientation. A positive angle indicates that the major axis of contact is oriented to the right. A negative angle indicates that the major axis of contact is oriented to the left. The full range is from -PI/2 radians (finger pointing fully left) to PI/2 radians (finger pointing fully right).
- For a stylus, the orientation indicates the direction in which the stylus is pointing in relation to the vertical axis of the current orientation of the screen. The range is from -PI radians to PI radians, where 0 is pointing up, -PI/2 radians is pointing left, -PI or PI radians is pointing down, and PI/2 radians is pointing right. See also [AXIS_TILT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TILT:kotlin.Int).

<br />

 Value: 8

**See Also**

- [#getOrientation(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getOrientation(kotlin.Int))
- [#getHistoricalOrientation(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalOrientation(kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#orientation](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#orientation:kotlin.Float) 

### AXIS_PRESSURE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_PRESSURE: Int
```

Axis constant: Pressure axis of a motion event.

<br />

- For a touch screen or touch pad, reports the approximate pressure applied to the surface by a finger or other tool. The value is normalized to a range from 0 (no pressure at all) to 1 (normal pressure), although values higher than 1 may be generated depending on the calibration of the input device.
- For a trackball, the value is set to 1 if the trackball button is pressed or 0 otherwise.
- For a mouse, the value is set to 1 if the primary mouse button is pressed or 0 otherwise.

<br />

 Value: 2

**See Also**

- [#getPressure(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure(kotlin.Int))
- [#getHistoricalPressure(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalPressure(kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#pressure](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#pressure:kotlin.Float) 

### AXIS_RELATIVE_X

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_RELATIVE_X: Int
```

Axis constant: The movement of x position of a motion event.

<br />

- For a mouse, reports a difference of x position between the previous position. This is useful when pointer is captured, in that case the mouse pointer doesn't change the location but this axis reports the difference which allows the app to see how the mouse is moved.

<br />

These values are relative to the state from the last sample, not accumulated, so developers should make sure to process this axis value for all batched historical samples. 

 Value: 27

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int)) 

### AXIS_RELATIVE_Y

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_RELATIVE_Y: Int
```

Axis constant: The movement of y position of a motion event.

This is similar to [AXIS_RELATIVE_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_RELATIVE_X:kotlin.Int) but for y-axis.

These values are relative to the state from the last sample, not accumulated, so developers should make sure to process this axis value for all batched historical samples. 

 Value: 28

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int)) 

### AXIS_RTRIGGER

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_RTRIGGER: Int
```

Axis constant: Right Trigger axis of a motion event.

<br />

- For a joystick, reports the absolute position of the right trigger control. The value is normalized to a range from 0.0 (released) to 1.0 (fully pressed).

<br />

 Value: 18

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_RUDDER

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_RUDDER: Int
```

Axis constant: Rudder axis of a motion event.

<br />

- For a joystick, reports the absolute position of the rudder control. The value is normalized to a range from -1.0 (turn left) to 1.0 (turn right).

<br />

 Value: 20

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_RX

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_RX: Int
```

Axis constant: X Rotation axis of a motion event.

<br />

- For a joystick, reports the absolute rotation angle about the X axis. The value is normalized to a range from -1.0 (counter-clockwise) to 1.0 (clockwise).

<br />

 Value: 12

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_RY

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_RY: Int
```

Axis constant: Y Rotation axis of a motion event.

<br />

- For a joystick, reports the absolute rotation angle about the Y axis. The value is normalized to a range from -1.0 (counter-clockwise) to 1.0 (clockwise).

<br />

 Value: 13

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_RZ

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_RZ: Int
```

Axis constant: Z Rotation axis of a motion event.

<br />

- For a joystick, reports the absolute rotation angle about the Z axis. The value is normalized to a range from -1.0 (counter-clockwise) to 1.0 (clockwise).*On game pads with two analog joysticks, this axis is often reinterpreted to report the absolute Y position of the second joystick instead.*

<br />

 Value: 14

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_SCROLL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_SCROLL: Int
```

Axis constant: Generic scroll axis of a motion event.

<br />

- Reports the relative movement of the generic scrolling device.

<br />

This axis should be used for scroll events that are neither strictly vertical nor horizontal. A good example would be the rotation of a rotary encoder input device. 

 Value: 26

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int)) 

### AXIS_SIZE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_SIZE: Int
```

Axis constant: Size axis of a motion event.

<br />

- For a touch screen or touch pad, reports the approximate size of the contact area in relation to the maximum detectable size for the device. The value is normalized to a range from 0 (smallest detectable size) to 1 (largest detectable size), although it is not a linear scale. The value of size can be used to determine fat touch events. To obtain calibrated size information, use [AXIS_TOUCH_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int) or [AXIS_TOOL_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int).

<br />

 Value: 3

**See Also**

- [#getSize(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize(kotlin.Int))
- [#getHistoricalSize(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalSize(kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#size](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#size:kotlin.Float) 

### AXIS_THROTTLE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_THROTTLE: Int
```

Axis constant: Throttle axis of a motion event.

<br />

- For a joystick, reports the absolute position of the throttle control. The value is normalized to a range from 0.0 (fully open) to 1.0 (fully closed).

<br />

 Value: 19

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_TILT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_TILT: Int
```

Axis constant: Tilt axis of a motion event.

<br />

- For a stylus, reports the tilt angle of the stylus in radians where 0 radians indicates that the stylus is being held perpendicular to the surface, and PI/2 radians indicates that the stylus is being held flat against the surface.

<br />

 Value: 25

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int)) 

### AXIS_TOOL_MAJOR

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_TOOL_MAJOR: Int
```

Axis constant: ToolMajor axis of a motion event.

<br />

- For a touch screen, reports the length of the major axis of an ellipse that represents the size of the approaching finger or tool used to make contact.
- For a touch pad, reports the length of the major axis of an ellipse that represents the size of the approaching finger or tool used to make contact. The units are device-dependent; use [InputDevice.getMotionRange(int)](https://developer.android.com/reference/kotlin/android/view/InputDevice#getMotionRange(kotlin.Int))to query the effective range of values.

<br />

When the touch is circular, the major and minor axis lengths will be equal to one another.

The tool size may be larger than the touch size since the tool may not be fully in contact with the touch sensor. 

 Value: 6

**See Also**

- [#getToolMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMajor(kotlin.Int))
- [#getHistoricalToolMajor(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMajor(kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#toolMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#toolMajor:kotlin.Float) 

### AXIS_TOOL_MINOR

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_TOOL_MINOR: Int
```

Axis constant: ToolMinor axis of a motion event.

<br />

- For a touch screen, reports the length of the minor axis of an ellipse that represents the size of the approaching finger or tool used to make contact.
- For a touch pad, reports the length of the minor axis of an ellipse that represents the size of the approaching finger or tool used to make contact. The units are device-dependent; use [InputDevice.getMotionRange(int)](https://developer.android.com/reference/kotlin/android/view/InputDevice#getMotionRange(kotlin.Int))to query the effective range of values.

<br />

When the touch is circular, the major and minor axis lengths will be equal to one another.

The tool size may be larger than the touch size since the tool may not be fully in contact with the touch sensor. 

 Value: 7

**See Also**

- [#getToolMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMinor(kotlin.Int))
- [#getHistoricalToolMinor(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMinor(kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#toolMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#toolMinor:kotlin.Float) 

### AXIS_TOUCH_MAJOR

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_TOUCH_MAJOR: Int
```

Axis constant: TouchMajor axis of a motion event.

<br />

- For a touch screen, reports the length of the major axis of an ellipse that represents the touch area at the point of contact. The units are display pixels.
- For a touch pad, reports the length of the major axis of an ellipse that represents the touch area at the point of contact. The units are device-dependent; use [InputDevice.getMotionRange(int)](https://developer.android.com/reference/kotlin/android/view/InputDevice#getMotionRange(kotlin.Int))to query the effective range of values.

<br />

 Value: 4

**See Also**

- [#getTouchMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMajor(kotlin.Int))
- [#getHistoricalTouchMajor(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMajor(kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#touchMajor](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#touchMajor:kotlin.Float) 

### AXIS_TOUCH_MINOR

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_TOUCH_MINOR: Int
```

Axis constant: TouchMinor axis of a motion event.

<br />

- For a touch screen, reports the length of the minor axis of an ellipse that represents the touch area at the point of contact. The units are display pixels.
- For a touch pad, reports the length of the minor axis of an ellipse that represents the touch area at the point of contact. The units are device-dependent; use [InputDevice.getMotionRange(int)](https://developer.android.com/reference/kotlin/android/view/InputDevice#getMotionRange(kotlin.Int))to query the effective range of values.

<br />

When the touch is circular, the major and minor axis lengths will be equal to one another. 

 Value: 5

**See Also**

- [#getTouchMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMinor(kotlin.Int))
- [#getHistoricalTouchMinor(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMinor(kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#touchMinor](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#touchMinor:kotlin.Float) 

### AXIS_VSCROLL

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_VSCROLL: Int
```

Axis constant: Vertical Scroll axis of a motion event.

<br />

- For a mouse, reports the relative movement of the vertical scroll wheel. The value is normalized to a range from -1.0 (down) to 1.0 (up).

<br />

This axis should be used to scroll views vertically. 

 Value: 9

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_WHEEL

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_WHEEL: Int
```

Axis constant: Wheel axis of a motion event.

<br />

- For a joystick, reports the absolute position of the steering wheel control. The value is normalized to a range from -1.0 (turn left) to 1.0 (turn right).

<br />

 Value: 21

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### AXIS_X

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_X: Int
```

Axis constant: X axis of a motion event.

<br />

- For a touch screen, reports the absolute X screen position of the center of the touch contact area. The units are display pixels.
- For a touch pad, reports the absolute X surface position of the center of the touch contact area. The units are device-dependent; use [InputDevice.getMotionRange(int)](https://developer.android.com/reference/kotlin/android/view/InputDevice#getMotionRange(kotlin.Int))to query the effective range of values.
- For a mouse, reports the absolute X screen position of the mouse pointer. The units are display pixels.
- For a trackball, reports the relative horizontal displacement of the trackball. The value is normalized to a range from -1.0 (left) to 1.0 (right).
- For a joystick, reports the absolute X position of the joystick. The value is normalized to a range from -1.0 (left) to 1.0 (right).

<br />

 Value: 0

**See Also**

- [#getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int))
- [#getHistoricalX(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalX(kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#x](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#x:kotlin.Float) 

### AXIS_Y

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_Y: Int
```

Axis constant: Y axis of a motion event.

<br />

- For a touch screen, reports the absolute Y screen position of the center of the touch contact area. The units are display pixels.
- For a touch pad, reports the absolute Y surface position of the center of the touch contact area. The units are device-dependent; use [InputDevice.getMotionRange(int)](https://developer.android.com/reference/kotlin/android/view/InputDevice#getMotionRange(kotlin.Int))to query the effective range of values.
- For a mouse, reports the absolute Y screen position of the mouse pointer. The units are display pixels.
- For a trackball, reports the relative vertical displacement of the trackball. The value is normalized to a range from -1.0 (up) to 1.0 (down).
- For a joystick, reports the absolute Y position of the joystick. The value is normalized to a range from -1.0 (up or far) to 1.0 (down or near).

<br />

 Value: 1

**See Also**

- [#getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int))
- [#getHistoricalY(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalY(kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#y](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#y:kotlin.Float) 

### AXIS_Z

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_Z: Int
```

Axis constant: Z axis of a motion event.

<br />

- For a joystick, reports the absolute Z position of the joystick. The value is normalized to a range from -1.0 (high) to 1.0 (low).*On game pads with two analog joysticks, this axis is often reinterpreted to report the absolute X position of the second joystick instead.*

<br />

 Value: 11

**See Also**

- [#getAxisValue(int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int))
- [#getHistoricalAxisValue(int, int, int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.MotionEvent.PointerCoords#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords#getAxisValue(kotlin.Int)) 

### BUTTON_BACK

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_BACK: Int
```

Button constant: Back button pressed (mouse back button).

The system may send a [KeyEvent.KEYCODE_BACK](https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_BACK:kotlin.Int) key press to the application when this button is pressed. 

 Value: 8

**See Also**

- [#getButtonState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState()) 

### BUTTON_FORWARD

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_FORWARD: Int
```

Button constant: Forward button pressed (mouse forward button).

The system may send a [KeyEvent.KEYCODE_FORWARD](https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_FORWARD:kotlin.Int) key press to the application when this button is pressed. 

 Value: 16

**See Also**

- [#getButtonState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState()) 

### BUTTON_PRIMARY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_PRIMARY: Int
```

Button constant: Primary button (left mouse button). This button constant is not set in response to simple touches with a finger or stylus tip. The user must actually push a button. 

 Value: 1

**See Also**

- [#getButtonState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState()) 

### BUTTON_SECONDARY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_SECONDARY: Int
```

Button constant: Secondary button (right mouse button). 

 Value: 2

**See Also**

- [#getButtonState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState()) 

### BUTTON_STYLUS_PRIMARY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_STYLUS_PRIMARY: Int
```

Button constant: Primary stylus button pressed. 

 Value: 32

**See Also**

- [#getButtonState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState()) 

### BUTTON_STYLUS_SECONDARY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_STYLUS_SECONDARY: Int
```

Button constant: Secondary stylus button pressed. 

 Value: 64

**See Also**

- [#getButtonState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState()) 

### BUTTON_TERTIARY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_TERTIARY: Int
```

Button constant: Tertiary button (middle mouse button). 

 Value: 4

**See Also**

- [#getButtonState](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState()) 

### CLASSIFICATION_AMBIGUOUS_GESTURE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLASSIFICATION_AMBIGUOUS_GESTURE: Int
```

Classification constant: Ambiguous gesture. The user's intent with respect to the current event stream is not yet determined. Gestural actions, such as scrolling, should be inhibited until the classification resolves to another value or the event stream ends. 

 Value: 1

**See Also**

- [#getClassification](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getClassification()) 

### CLASSIFICATION_DEEP_PRESS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLASSIFICATION_DEEP_PRESS: Int
```

Classification constant: Deep press. The current event stream represents the user intentionally pressing harder on the screen. This classification type should be used to accelerate the long press behaviour. 

 Value: 2

**See Also**

- [#getClassification](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getClassification()) 

### CLASSIFICATION_NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLASSIFICATION_NONE: Int
```

Classification constant: None. No additional information is available about the current motion event stream. 

 Value: 0

**See Also**

- [#getClassification](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getClassification()) 

### CLASSIFICATION_PINCH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLASSIFICATION_PINCH: Int
```

Classification constant: touchpad pinch. The current event stream represents the user pinching with two fingers on a touchpad. The gesture is centered around the current cursor position. 

 Value: 5

**See Also**

- [#getClassification](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getClassification()) 

### CLASSIFICATION_TWO_FINGER_SWIPE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLASSIFICATION_TWO_FINGER_SWIPE: Int
```

Classification constant: touchpad scroll. The current event stream represents the user scrolling with two fingers on a touchpad. 

 Value: 3

**See Also**

- [#getClassification](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getClassification()) 

### EDGE_BOTTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDGE_BOTTOM: Int
```

Flag indicating the motion event intersected the bottom edge of the screen. 

 Value: 2

### EDGE_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDGE_LEFT: Int
```

Flag indicating the motion event intersected the left edge of the screen. 

 Value: 4

### EDGE_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDGE_RIGHT: Int
```

Flag indicating the motion event intersected the right edge of the screen. 

 Value: 8

### EDGE_TOP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDGE_TOP: Int
```

Flag indicating the motion event intersected the top edge of the screen. 

 Value: 1

### FLAG_CANCELED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CANCELED: Int
```

This flag is only set for events with [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int) and [ACTION_CANCEL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int). It indicates that the pointer going up was an unintentional user touch. When FLAG_CANCELED is set, the typical actions that occur in response for a pointer going up (such as click handlers, end of drawing) should be aborted. This flag is typically set when the user was accidentally touching the screen, such as by gripping the device, or placing the palm on the screen. 

 Value: 32

**See Also**

- [#ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int)
- [#ACTION_CANCEL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_CANCEL:kotlin.Int) 

### FLAG_WINDOW_IS_OBSCURED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_WINDOW_IS_OBSCURED: Int
```

This flag indicates that the window that received this motion event is partly or wholly obscured by another visible window above it and the event directly passed through the obscured area. A security sensitive application can check this flag to identify situations in which a malicious application may have covered up part of its content for the purpose of misleading the user or hijacking touches. An appropriate response might be to drop the suspect touches or to take additional precautions to confirm the user's actual intent. 

 Value: 1

### FLAG_WINDOW_IS_PARTIALLY_OBSCURED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_WINDOW_IS_PARTIALLY_OBSCURED: Int
```

This flag indicates that the window that received this motion event is partly or wholly obscured by another visible window above it and the event did not directly pass through the obscured area. A security sensitive application can check this flag to identify situations in which a malicious application may have covered up part of its content for the purpose of misleading the user or hijacking touches. An appropriate response might be to drop the suspect touches or to take additional precautions to confirm the user's actual intent. Unlike FLAG_WINDOW_IS_OBSCURED, this is only true if the window that received this event is obstructed in areas other than the touched location. 

 Value: 2

### INVALID_POINTER_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_POINTER_ID: Int
```

An invalid pointer id. This value (-1) can be used as a placeholder to indicate that a pointer id has not been assigned or is not available. It cannot appear as a pointer id inside a [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#). 

 Value: -1

### TOOL_TYPE_ERASER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOOL_TYPE_ERASER: Int
```

Tool type constant: The tool is an eraser or a stylus being used in an inverted posture. 

 Value: 4

**See Also**

- [#getToolType](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolType(kotlin.Int)) 

### TOOL_TYPE_FINGER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOOL_TYPE_FINGER: Int
```

Tool type constant: The tool is a finger. 

 Value: 1

**See Also**

- [#getToolType](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolType(kotlin.Int)) 

### TOOL_TYPE_MOUSE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOOL_TYPE_MOUSE: Int
```

Tool type constant: The tool is a mouse. 

 Value: 3

**See Also**

- [#getToolType](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolType(kotlin.Int)) 

### TOOL_TYPE_STYLUS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOOL_TYPE_STYLUS: Int
```

Tool type constant: The tool is a stylus. 

 Value: 2

**See Also**

- [#getToolType](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolType(kotlin.Int)) 

### TOOL_TYPE_UNKNOWN

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOOL_TYPE_UNKNOWN: Int
```

Tool type constant: Unknown tool type. This constant is used when the tool type is not known or is not relevant, such as for a trackball or other non-pointing device. 

 Value: 0

**See Also**

- [#getToolType](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolType(kotlin.Int))

## Public methods

### actionToString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun actionToString(action: Int): String!
```

Returns a string that represents the symbolic name of the specified unmasked action such as "ACTION_DOWN", "ACTION_POINTER_DOWN(3)" or an equivalent numeric constant such as "35" if unknown.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unmasked action. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The symbolic name of the specified action. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAction()> 

### addBatch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addBatch(
    eventTime: Long, 
    pointerCoords: Array<MotionEvent.PointerCoords!>!, 
    metaState: Int
): Unit
```

Add a new movement to the batch of movements in this event. The event's current location, position and size is updated to the new values. The current values in the event are added to a list of historical values. Only applies to [ACTION_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int) or [ACTION_HOVER_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_MOVE:kotlin.Int) events.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time stamp (in ms) for this data. |
| `pointerCoords` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!\>!:The new pointer coordinates. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Meta key state. |

### addBatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addBatch(
    eventTime: Long, 
    x: Float, 
    y: Float, 
    pressure: Float, 
    size: Float, 
    metaState: Int
): Unit
```

Add a new movement to the batch of movements in this event. The event's current location, position and size is updated to the new values. The current values in the event are added to a list of historical values. Only applies to [ACTION_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_MOVE:kotlin.Int) or [ACTION_HOVER_MOVE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_HOVER_MOVE:kotlin.Int) events.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------|
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time stamp (in ms) for this data. |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new X position. |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new Y position. |
| `pressure` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new pressure. |
| `size` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new size. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Meta key state. |

### axisFromString

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun axisFromString(symbolicName: String!): Int
```

Gets an axis by its symbolic name such as "AXIS_X" or an equivalent numeric constant such as "42".

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------|
| `symbolicName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The symbolic name of the axis. |

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The axis or -1 if not found. |

**See Also**

- [android.view.KeyEvent#keyCodeToString(int)](https://developer.android.com/reference/kotlin/android/view/KeyEvent#keyCodeToString(kotlin.Int)) 

### axisToString

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun axisToString(axis: Int): String!
```

Returns a string that represents the symbolic name of the specified axis such as "AXIS_X" or an equivalent numeric constant such as "42" if unknown.

| Parameters ||
|--------|--------------------------------------------------------------------------------------|
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The axis. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The symbolic name of the specified axis. |

### findPointerIndex

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun findPointerIndex(pointerId: Int): Int
```

Given a pointer identifier, find the index of its data in the event.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------|
| `pointerId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The identifier of the pointer to be found. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns either the index of the pointer (for use with [getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int))et al.), or -1 if there is no data available for that pointer identifier. |

### getAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAction(): Int
```

Return the kind of action being performed. Consider using [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked())and [getActionIndex](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionIndex())to retrieve the separate masked action and pointer index.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The action, such as [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) or the combination of [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int) with a shifted pointer index. |

### getActionButton

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActionButton(): Int
```

Gets which button has been modified during a press or release action. For actions other than [ACTION_BUTTON_PRESS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_BUTTON_PRESS:kotlin.Int) and [ACTION_BUTTON_RELEASE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_BUTTON_RELEASE:kotlin.Int) the returned value is undefined. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getButtonState()> 

### getActionIndex

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActionIndex(): Int
```

For [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int) or [ACTION_POINTER_UP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_UP:kotlin.Int) as returned by [getActionMasked](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionMasked()), this returns the associated pointer index. The index may be used with [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int)), [getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int)), [getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int)), [getPressure(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure(kotlin.Int)), and [getSize(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize(kotlin.Int))to get information about the pointer that has gone down or up.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index associated with the action. |

### getActionMasked

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActionMasked(): Int
```

Return the masked action being performed, without pointer index information. Use [getActionIndex](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getActionIndex())to return the index associated with pointer actions.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The action, such as [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) or [ACTION_POINTER_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_POINTER_DOWN:kotlin.Int). |

### getAxisValue

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAxisValue(axis: Int): Float
```

[getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The axis identifier for the axis value to retrieve. |

**See Also**

- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int)
- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getAxisValue

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAxisValue(
    axis: Int, 
    pointerIndex: Int
): Float
```

Returns the value of the requested axis for the given pointer*index* (use [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int))to find the pointer identifier for this index).

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The axis identifier for the axis value to retrieve. |
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The value of the axis, or 0 if the axis is not available. |

**See Also**

- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int)
- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getButtonState

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getButtonState(): Int
```

Gets the state of all buttons that are pressed such as a mouse or stylus button.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The button state. |

**See Also**

- [#BUTTON_PRIMARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_PRIMARY:kotlin.Int)
- [#BUTTON_SECONDARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_SECONDARY:kotlin.Int)
- [#BUTTON_TERTIARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_TERTIARY:kotlin.Int)
- [#BUTTON_FORWARD](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_FORWARD:kotlin.Int)
- [#BUTTON_BACK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_BACK:kotlin.Int)
- [#BUTTON_STYLUS_PRIMARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_STYLUS_PRIMARY:kotlin.Int)
- [#BUTTON_STYLUS_SECONDARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_STYLUS_SECONDARY:kotlin.Int) 

### getClassification

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClassification(): Int
```

Returns the classification for the current gesture. The classification may change as more events become available for the same gesture.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.MotionEvent#CLASSIFICATION_NONE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_NONE:kotlin.Int), [android.view.MotionEvent#CLASSIFICATION_AMBIGUOUS_GESTURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_AMBIGUOUS_GESTURE:kotlin.Int), [android.view.MotionEvent#CLASSIFICATION_DEEP_PRESS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_DEEP_PRESS:kotlin.Int), [android.view.MotionEvent#CLASSIFICATION_TWO_FINGER_SWIPE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_TWO_FINGER_SWIPE:kotlin.Int), android.view.MotionEvent.CLASSIFICATION_MULTI_FINGER_SWIPE, or [android.view.MotionEvent#CLASSIFICATION_PINCH](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_PINCH:kotlin.Int) |

**See Also**

- [#CLASSIFICATION_NONE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_NONE:kotlin.Int)
- [#CLASSIFICATION_AMBIGUOUS_GESTURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_AMBIGUOUS_GESTURE:kotlin.Int)
- [#CLASSIFICATION_DEEP_PRESS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_DEEP_PRESS:kotlin.Int) 

### getDeviceId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceId(): Int
```

Gets the id for the device that this event came from. An id of zero indicates that the event didn't come from a physical device and maps to the default keymap. The other numbers are arbitrary and you shouldn't depend on the values.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The device id. |

### getDownTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDownTime(): Long
```

Returns the time (in ms) when the user originally pressed down to start a stream of position events. 

### getEdgeFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEdgeFlags(): Int
```

Returns a bitfield indicating which edges, if any, were touched by this MotionEvent. For touch events, clients can use this to determine if the user's finger was touching the edge of the display. This property is only set for [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int) events. 
**See Also**

- [#EDGE_LEFT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#EDGE_LEFT:kotlin.Int)
- [#EDGE_TOP](https://developer.android.com/reference/kotlin/android/view/MotionEvent#EDGE_TOP:kotlin.Int)
- [#EDGE_RIGHT](https://developer.android.com/reference/kotlin/android/view/MotionEvent#EDGE_RIGHT:kotlin.Int)
- [#EDGE_BOTTOM](https://developer.android.com/reference/kotlin/android/view/MotionEvent#EDGE_BOTTOM:kotlin.Int) 

### getEventTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventTime(): Long
```

Retrieve the time this event occurred, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Returns the time this event occurred, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base. |

### getEventTimeNanos

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventTimeNanos(): Long
```

Retrieve the time this event occurred, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base but with nanosecond precision.

The value is in nanosecond precision but it may not have nanosecond accuracy.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Returns the time this event occurred, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base but with nanosecond precision. |

### getFlags

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Gets the motion event flags. 
**See Also**

- [#FLAG_WINDOW_IS_OBSCURED](https://developer.android.com/reference/kotlin/android/view/MotionEvent#FLAG_WINDOW_IS_OBSCURED:kotlin.Int) 

### getHistoricalAxisValue

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalAxisValue(
    axis: Int, 
    pos: Int
): Float
```

[getHistoricalAxisValue(int,int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalAxisValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The axis identifier for the axis value to retrieve. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int))
- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int)
- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getHistoricalAxisValue

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalAxisValue(
    axis: Int, 
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns the historical value of the requested axis, as per [getAxisValue(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int,%20kotlin.Int)), occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The axis identifier for the axis value to retrieve. |
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The value of the axis, or 0 if the axis is not available. |

**See Also**

- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int)
- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getHistoricalEventTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalEventTime(pos: Int): Long
```

Returns the time that a historical movement occurred between this event and the previous event, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base.

This only applies to ACTION_MOVE events.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Returns the time that a historical movement occurred between this event and the previous event, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base. |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getEventTime](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getEventTime()) 

### getHistoricalEventTimeNanos

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalEventTimeNanos(pos: Int): Long
```

Returns the time that a historical movement occurred between this event and the previous event, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base but with nanosecond (instead of millisecond) precision.

This only applies to ACTION_MOVE events.

The value is in nanosecond precision but it may not have nanosecond accuracy.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Returns the time that a historical movement occurred between this event and the previous event, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base but with nanosecond (instead of millisecond) precision. |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getEventTime](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getEventTime()) 

### getHistoricalOrientation

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalOrientation(pos: Int): Float
```

[getHistoricalOrientation(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalOrientation(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getOrientation()>
- [#AXIS_ORIENTATION](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_ORIENTATION:kotlin.Int) 

### getHistoricalOrientation

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalOrientation(
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns a historical orientation coordinate, as per [getOrientation(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getOrientation(kotlin.Int)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getOrientation(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getOrientation(kotlin.Int))
- [#AXIS_ORIENTATION](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_ORIENTATION:kotlin.Int) 

### getHistoricalPointerCoords

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalPointerCoords(
    pointerIndex: Int, 
    pos: Int, 
    outPointerCoords: MotionEvent.PointerCoords!
): Unit
```

Populates a [PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) object with historical pointer coordinate data, as per [getPointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCoords(kotlin.Int,%20android.view.MotionEvent.PointerCoords)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |
| `outPointerCoords` | [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!:The pointer coordinate object to populate. |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getPointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCoords(kotlin.Int,%20android.view.MotionEvent.PointerCoords))
- [android.view.MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) 

### getHistoricalPressure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalPressure(pos: Int): Float
```

[getHistoricalPressure(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalPressure(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure()>
- [#AXIS_PRESSURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_PRESSURE:kotlin.Int) 

### getHistoricalPressure

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalPressure(
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns a historical pressure coordinate, as per [getPressure(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure(kotlin.Int)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getPressure(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure(kotlin.Int))
- [#AXIS_PRESSURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_PRESSURE:kotlin.Int) 

### getHistoricalSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalSize(pos: Int): Float
```

[getHistoricalSize(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalSize(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize()>
- [#AXIS_SIZE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_SIZE:kotlin.Int) 

### getHistoricalSize

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalSize(
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns a historical size coordinate, as per [getSize(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize(kotlin.Int)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getSize(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize(kotlin.Int))
- [#AXIS_SIZE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_SIZE:kotlin.Int) 

### getHistoricalToolMajor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalToolMajor(pos: Int): Float
```

[getHistoricalToolMajor(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMajor(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMajor()>
- [#AXIS_TOOL_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int) 

### getHistoricalToolMajor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalToolMajor(
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns a historical tool major axis coordinate, as per [getToolMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMajor(kotlin.Int)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getToolMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMajor(kotlin.Int))
- [#AXIS_TOOL_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int) 

### getHistoricalToolMinor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalToolMinor(pos: Int): Float
```

[getHistoricalToolMinor(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalToolMinor(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMinor()>
- [#AXIS_TOOL_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MINOR:kotlin.Int) 

### getHistoricalToolMinor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalToolMinor(
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns a historical tool minor axis coordinate, as per [getToolMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMinor(kotlin.Int)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getToolMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMinor(kotlin.Int))
- [#AXIS_TOOL_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MINOR:kotlin.Int) 

### getHistoricalTouchMajor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalTouchMajor(pos: Int): Float
```

[getHistoricalTouchMajor(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMajor(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMajor()>
- [#AXIS_TOUCH_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int) 

### getHistoricalTouchMajor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalTouchMajor(
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns a historical touch major axis coordinate, as per [getTouchMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMajor(kotlin.Int)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getTouchMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMajor(kotlin.Int))
- [#AXIS_TOUCH_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int) 

### getHistoricalTouchMinor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalTouchMinor(pos: Int): Float
```

[getHistoricalTouchMinor(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalTouchMinor(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMinor()>
- [#AXIS_TOUCH_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MINOR:kotlin.Int) 

### getHistoricalTouchMinor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalTouchMinor(
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns a historical touch minor axis coordinate, as per [getTouchMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMinor(kotlin.Int)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getTouchMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMinor(kotlin.Int))
- [#AXIS_TOUCH_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MINOR:kotlin.Int) 

### getHistoricalX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalX(pos: Int): Float
```

[getHistoricalX(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalX(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX()>
- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int) 

### getHistoricalX

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalX(
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns a historical X coordinate, as per [getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int))
- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int) 

### getHistoricalY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalY(pos: Int): Float
```

[getHistoricalY(int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistoricalY(kotlin.Int,%20kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY()>
- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getHistoricalY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistoricalY(
    pointerIndex: Int, 
    pos: Int
): Float
```

Returns a historical Y coordinate, as per [getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int)), that occurred between this event and the previous event for the given pointer. Only applies to ACTION_MOVE events.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which historical value to return; must be less than [getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize()) |

**See Also**

- [#getHistorySize](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getHistorySize())
- [#getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int))
- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getHistorySize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHistorySize(): Int
```

Returns the number of historical points in this event. These are movements that have occurred between this event and the previous event. This only applies to ACTION_MOVE events -- all other actions will have a size of 0.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns the number of historical points in the event. |

### getMetaState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetaState(): Int
```

Returns the state of any meta / modifier keys that were in effect when the event was generated. This is the same values as those returned by [KeyEvent.getMetaState](https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an integer in which each bit set to 1 represents a pressed meta key |

**See Also**

- [android.view.KeyEvent#getMetaState()](https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()) 

### getOrientation

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOrientation(): Float
```

[getOrientation(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getOrientation(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). 
**See Also**

- [#AXIS_ORIENTATION](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_ORIENTATION:kotlin.Int) 

### getOrientation

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOrientation(pointerIndex: Int): Float
```

Returns the value of [AXIS_ORIENTATION](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_ORIENTATION:kotlin.Int) for the given pointer*index*.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

**See Also**

- [#AXIS_ORIENTATION](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_ORIENTATION:kotlin.Int) 

### getPointerCoords

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPointerCoords(
    pointerIndex: Int, 
    outPointerCoords: MotionEvent.PointerCoords!
): Unit
```

Populates a [PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) object with pointer coordinate data for the specified pointer index.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `outPointerCoords` | [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!:The pointer coordinate object to populate. |

**See Also**

- [android.view.MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) 

### getPointerCount

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPointerCount(): Int
```

The number of pointers of data contained in this event. Always \>= 1. 

### getPointerId

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPointerId(pointerIndex: Int): Int
```

Return the pointer identifier associated with a particular pointer data index in this event. The identifier tells you the actual pointer number associated with the data, accounting for individual pointers going up and down since the start of the current gesture.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

### getPointerProperties

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPointerProperties(
    pointerIndex: Int, 
    outPointerProperties: MotionEvent.PointerProperties!
): Unit
```

Populates a [PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties) object with pointer properties for the specified pointer index.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |
| `outPointerProperties` | [MotionEvent.PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties)!:The pointer properties object to populate. |

**See Also**

- [android.view.MotionEvent.PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties) 

### getPressure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPressure(): Float
```

[getPressure(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPressure(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). 
**See Also**

- [#AXIS_PRESSURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_PRESSURE:kotlin.Int) 

### getPressure

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPressure(pointerIndex: Int): Float
```

Returns the value of [AXIS_PRESSURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_PRESSURE:kotlin.Int) for the given pointer*index*.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

**See Also**

- [#AXIS_PRESSURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_PRESSURE:kotlin.Int) 

### getRawX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRawX(): Float
```

Equivalent to [getRawX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getRawX(kotlin.Int))for pointer index 0 (regardless of the pointer identifier).

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The X coordinate of the first pointer index in the coordinate space of the device display. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX()>
- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int) 

### getRawX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRawX(pointerIndex: Int): Float
```

Returns the X coordinate of the pointer referenced by`pointerIndex`for this motion event. The coordinate is in the coordinate space of the device display, irrespective of system decorations and whether or not the system is in multi-window mode. If the app spans multiple screens in a multiple-screen environment, the coordinate space includes all of the spanned screens.

In multi-window mode, the coordinate space extends beyond the bounds of the app window to encompass the entire display area. For example, if the motion event occurs in the right-hand window of split-screen mode in landscape orientation, the left edge of the screen---not the left edge of the window---is the origin from which the X coordinate is calculated.

In multiple-screen scenarios, the coordinate space can span screens. For example, if the app is spanning both screens of a dual-screen device, and the motion event occurs on the right-hand screen, the X coordinate is calculated from the left edge of the left-hand screen to the point of the motion event on the right-hand screen. When the app is restricted to a single screen in a multiple-screen environment, the coordinate space includes only the screen on which the app is running.

Use [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int))to get the pointer identifier for the pointer referenced by`pointerIndex`.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the pointer for which the X coordinate is returned. May be a value in the range of 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())- 1. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The X coordinate of the pointer referenced by`pointerIndex`for this motion event. The unit is pixels. The value may contain a fractional portion for devices that are subpixel precise. |

**See Also**

- [#getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int))
- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int) 

### getRawY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRawY(): Float
```

Equivalent to [getRawY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getRawY(kotlin.Int))for pointer index 0 (regardless of the pointer identifier).

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The Y coordinate of the first pointer index in the coordinate space of the device display. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY()>
- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getRawY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRawY(pointerIndex: Int): Float
```

Returns the Y coordinate of the pointer referenced by`pointerIndex`for this motion event. The coordinate is in the coordinate space of the device display, irrespective of system decorations and whether or not the system is in multi-window mode. If the app spans multiple screens in a multiple-screen environment, the coordinate space includes all of the spanned screens.

In multi-window mode, the coordinate space extends beyond the bounds of the app window to encompass the entire device screen. For example, if the motion event occurs in the lower window of split-screen mode in portrait orientation, the top edge of the screen---not the top edge of the window---is the origin from which the Y coordinate is determined.

In multiple-screen scenarios, the coordinate space can span screens. For example, if the app is spanning both screens of a dual-screen device that's rotated 90 degrees, and the motion event occurs on the lower screen, the Y coordinate is calculated from the top edge of the upper screen to the point of the motion event on the lower screen. When the app is restricted to a single screen in a multiple-screen environment, the coordinate space includes only the screen on which the app is running.

Use [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int))to get the pointer identifier for the pointer referenced by`pointerIndex`.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the pointer for which the Y coordinate is returned. May be a value in the range of 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())- 1. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The Y coordinate of the pointer referenced by`pointerIndex`for this motion event. The unit is pixels. The value may contain a fractional portion for devices that are subpixel precise. |

**See Also**

- [#getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int))
- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSize(): Float
```

[getSize(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSize(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). 
**See Also**

- [#AXIS_SIZE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_SIZE:kotlin.Int) 

### getSize

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSize(pointerIndex: Int): Float
```

Returns the value of [AXIS_SIZE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_SIZE:kotlin.Int) for the given pointer*index*.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

**See Also**

- [#AXIS_SIZE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_SIZE:kotlin.Int) 

### getSource

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSource(): Int
```

Gets the source of the event.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The event source or [InputDevice.SOURCE_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_UNKNOWN:kotlin.Int) if unknown. |

### getToolMajor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getToolMajor(): Float
```

[getToolMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMajor(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). 
**See Also**

- [#AXIS_TOOL_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int) 

### getToolMajor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getToolMajor(pointerIndex: Int): Float
```

Returns the value of [AXIS_TOOL_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int) for the given pointer*index*.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

**See Also**

- [#AXIS_TOOL_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MAJOR:kotlin.Int) 

### getToolMinor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getToolMinor(): Float
```

[getToolMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getToolMinor(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). 
**See Also**

- [#AXIS_TOOL_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MINOR:kotlin.Int) 

### getToolMinor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getToolMinor(pointerIndex: Int): Float
```

Returns the value of [AXIS_TOOL_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MINOR:kotlin.Int) for the given pointer*index*.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

**See Also**

- [#AXIS_TOOL_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOOL_MINOR:kotlin.Int) 

### getToolType

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getToolType(pointerIndex: Int): Int
```

Gets the tool type of a pointer for the given pointer index. The tool type indicates the type of tool used to make contact such as a finger or stylus, if known.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The tool type of the pointer. Value is [android.view.MotionEvent#TOOL_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_UNKNOWN:kotlin.Int), [android.view.MotionEvent#TOOL_TYPE_FINGER](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_FINGER:kotlin.Int), [android.view.MotionEvent#TOOL_TYPE_STYLUS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_STYLUS:kotlin.Int), [android.view.MotionEvent#TOOL_TYPE_MOUSE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_MOUSE:kotlin.Int), [android.view.MotionEvent#TOOL_TYPE_ERASER](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_ERASER:kotlin.Int), or android.view.MotionEvent.TOOL_TYPE_PALM |

**See Also**

- [#TOOL_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_UNKNOWN:kotlin.Int)
- [#TOOL_TYPE_FINGER](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_FINGER:kotlin.Int)
- [#TOOL_TYPE_STYLUS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_STYLUS:kotlin.Int)
- [#TOOL_TYPE_MOUSE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#TOOL_TYPE_MOUSE:kotlin.Int) 

### getTouchMajor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTouchMajor(): Float
```

[getTouchMajor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMajor(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). 
**See Also**

- [#AXIS_TOUCH_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int) 

### getTouchMajor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTouchMajor(pointerIndex: Int): Float
```

Returns the value of [AXIS_TOUCH_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int) for the given pointer*index*.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

**See Also**

- [#AXIS_TOUCH_MAJOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MAJOR:kotlin.Int) 

### getTouchMinor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTouchMinor(): Float
```

[getTouchMinor(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getTouchMinor(kotlin.Int))for the first pointer index (may be an arbitrary pointer identifier). 
**See Also**

- [#AXIS_TOUCH_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MINOR:kotlin.Int) 

### getTouchMinor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTouchMinor(pointerIndex: Int): Float
```

Returns the value of [AXIS_TOUCH_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MINOR:kotlin.Int) for the given pointer*index*.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Raw index of pointer to retrieve. Value may be from 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())-1. |

**See Also**

- [#AXIS_TOUCH_MINOR](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_TOUCH_MINOR:kotlin.Int) 

### getX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getX(): Float
```

Equivalent to [getX(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getX(kotlin.Int))for pointer index 0 (regardless of the pointer identifier).

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The X coordinate of the first pointer index in the coordinate space of the view that received this motion event. |

**See Also**

- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int) 

### getX

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getX(pointerIndex: Int): Float
```

Returns the X coordinate of the pointer referenced by`pointerIndex`for this motion event. The coordinate is in the coordinate space of the view that received this motion event.

Use [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int))to get the pointer identifier for the pointer referenced by`pointerIndex`.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the pointer for which the X coordinate is returned. May be a value in the range of 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())- 1. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The X coordinate of the pointer referenced by`pointerIndex`for this motion event. The unit is pixels. The value may contain a fractional portion for devices that are subpixel precise. |

**See Also**

- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int) 

### getXPrecision

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getXPrecision(): Float
```

Return the precision of the X coordinates being reported. You can multiply this number with #getX to find the actual hardware value of the X coordinate.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Returns the precision of X coordinates being reported. |

**See Also**

- [#AXIS_X](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_X:kotlin.Int) 

### getY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getY(): Float
```

Equivalent to [getY(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getY(kotlin.Int))for pointer index 0 (regardless of the pointer identifier).

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The Y coordinate of the first pointer index in the coordinate space of the view that received this motion event. |

**See Also**

- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getY(pointerIndex: Int): Float
```

Returns the Y coordinate of the pointer referenced by`pointerIndex`for this motion event. The coordinate is in the coordinate space of the view that received this motion event.

Use [getPointerId(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerId(kotlin.Int))to get the pointer identifier for the pointer referenced by`pointerIndex`.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pointerIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the pointer for which the Y coordinate is returned. May be a value in the range of 0 (the first pointer that is down) to [getPointerCount()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getPointerCount())- 1. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The Y coordinate of the pointer referenced by`pointerIndex`for this motion event. The unit is pixels. The value may contain a fractional portion for devices that are subpixel precise. |

**See Also**

- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### getYPrecision

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getYPrecision(): Float
```

Return the precision of the Y coordinates being reported. You can multiply this number with #getY to find the actual hardware value of the Y coordinate.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Returns the precision of Y coordinates being reported. |

**See Also**

- [#AXIS_Y](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_Y:kotlin.Int) 

### isButtonPressed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isButtonPressed(button: Int): Boolean
```

Checks if a mouse or stylus button (or combination of buttons) is pressed.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `button` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Button (or combination of buttons). |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if specified buttons are pressed. |

**See Also**

- [#BUTTON_PRIMARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_PRIMARY:kotlin.Int)
- [#BUTTON_SECONDARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_SECONDARY:kotlin.Int)
- [#BUTTON_TERTIARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_TERTIARY:kotlin.Int)
- [#BUTTON_FORWARD](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_FORWARD:kotlin.Int)
- [#BUTTON_BACK](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_BACK:kotlin.Int)
- [#BUTTON_STYLUS_PRIMARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_STYLUS_PRIMARY:kotlin.Int)
- [#BUTTON_STYLUS_SECONDARY](https://developer.android.com/reference/kotlin/android/view/MotionEvent#BUTTON_STYLUS_SECONDARY:kotlin.Int) 

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(other: MotionEvent!): MotionEvent!
```

Create a new MotionEvent, copying from an existing one. 

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    x: Float, 
    y: Float, 
    pressure: Float, 
    size: Float, 
    metaState: Int, 
    xPrecision: Float, 
    yPrecision: Float, 
    deviceId: Int, 
    edgeFlags: Int
): MotionEvent!
```

Create a new MotionEvent, filling in all of the basic values that define the motion.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when the user originally pressed down to start a stream of position events. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when this specific event was generated. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The kind of action being performed, such as [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int). |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of this event. |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of this event. |
| `pressure` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The current pressure of this event. The pressure generally ranges from 0 (no pressure at all) to 1 (normal pressure), however values higher than 1 may be generated depending on the calibration of the input device. |
| `size` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A scaled value of the approximate size of the area being pressed when touched with the finger. The actual value in pixels corresponding to the finger touch is normalized with a device specific range of values and scaled to a value between 0 and 1. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The state of any meta / modifier keys that were in effect when the event was generated. |
| `xPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the X coordinate being reported. |
| `yPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the Y coordinate being reported. |
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID for the device that this event came from. An ID of zero indicates that the event didn't come from a physical device; other numbers are arbitrary and you shouldn't depend on the values. |
| `edgeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitfield indicating which edges, if any, were touched by this MotionEvent. |

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    x: Float, 
    y: Float, 
    metaState: Int
): MotionEvent!
```

Create a new MotionEvent, filling in a subset of the basic motion values. Those not specified here are: device id (always 0), pressure and size (always 1), x and y precision (always 1), and edgeFlags (always 0).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when the user originally pressed down to start a stream of position events. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when this specific event was generated. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The kind of action being performed, such as [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int). |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of this event. |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of this event. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The state of any meta / modifier keys that were in effect when the event was generated. |

### obtain

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    pointerCount: Int, 
    pointerProperties: Array<MotionEvent.PointerProperties!>!, 
    pointerCoords: Array<MotionEvent.PointerCoords!>!, 
    metaState: Int, 
    buttonState: Int, 
    xPrecision: Float, 
    yPrecision: Float, 
    deviceId: Int, 
    edgeFlags: Int, 
    source: Int, 
    flags: Int
): MotionEvent!
```

Create a new MotionEvent, filling in all of the basic values that define the motion.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when the user originally pressed down to start a stream of position events. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when this specific event was generated. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The kind of action being performed, such as [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int). |
| `pointerCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of pointers that will be in this event. |
| `pointerProperties` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MotionEvent.PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties)!\>!:An array of*pointerCount* values providing a [PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties) property object for each pointer, which must include the pointer identifier. |
| `pointerCoords` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!\>!:An array of*pointerCount* values providing a [PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) coordinate object for each pointer. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The state of any meta / modifier keys that were in effect when the event was generated. |
| `buttonState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The state of buttons that are pressed. |
| `xPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the X coordinate being reported. |
| `yPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the Y coordinate being reported. |
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID for the device that this event came from. An ID of zero indicates that the event didn't come from a physical device; other numbers are arbitrary and you shouldn't depend on the values. |
| `edgeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitfield indicating which edges, if any, were touched by this MotionEvent. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The source of this event. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The motion event flags. |

### obtain

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    pointerCount: Int, 
    pointerProperties: Array<MotionEvent.PointerProperties!>, 
    pointerCoords: Array<MotionEvent.PointerCoords!>, 
    metaState: Int, 
    buttonState: Int, 
    xPrecision: Float, 
    yPrecision: Float, 
    deviceId: Int, 
    edgeFlags: Int, 
    source: Int, 
    displayId: Int, 
    flags: Int, 
    classification: Int
): MotionEvent?
```

Create a new MotionEvent, filling in all of the basic values that define the motion.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when the user originally pressed down to start a stream of position events. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when this specific event was generated. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The kind of action being performed, such as [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int). |
| `pointerCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of pointers that will be in this event. |
| `pointerProperties` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MotionEvent.PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties)!\>:An array of*pointerCount* values providing a [PointerProperties](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerProperties) property object for each pointer, which must include the pointer identifier. This value cannot be`null`. |
| `pointerCoords` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!\>:An array of*pointerCount* values providing a [PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) coordinate object for each pointer. This value cannot be`null`. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The state of any meta / modifier keys that were in effect when the event was generated. |
| `buttonState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The state of buttons that are pressed. |
| `xPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the X coordinate being reported. |
| `yPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the Y coordinate being reported. |
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID for the device that this event came from. An ID of zero indicates that the event didn't come from a physical device; other numbers are arbitrary and you shouldn't depend on the values. |
| `edgeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitfield indicating which edges, if any, were touched by this MotionEvent. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The source of this event. |
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The display ID associated with this event. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The motion event flags. |
| `classification` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The classification to give this event. Value is [android.view.MotionEvent#CLASSIFICATION_NONE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_NONE:kotlin.Int), [android.view.MotionEvent#CLASSIFICATION_AMBIGUOUS_GESTURE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_AMBIGUOUS_GESTURE:kotlin.Int), [android.view.MotionEvent#CLASSIFICATION_DEEP_PRESS](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_DEEP_PRESS:kotlin.Int), [android.view.MotionEvent#CLASSIFICATION_TWO_FINGER_SWIPE](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_TWO_FINGER_SWIPE:kotlin.Int), android.view.MotionEvent.CLASSIFICATION_MULTI_FINGER_SWIPE, or [android.view.MotionEvent#CLASSIFICATION_PINCH](https://developer.android.com/reference/kotlin/android/view/MotionEvent#CLASSIFICATION_PINCH:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent#)? | This value may be`null`. |

### obtain

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    pointerCount: Int, 
    x: Float, 
    y: Float, 
    pressure: Float, 
    size: Float, 
    metaState: Int, 
    xPrecision: Float, 
    yPrecision: Float, 
    deviceId: Int, 
    edgeFlags: Int
): MotionEvent!
```

**Deprecated:** *Use [obtain(long,long,int,float,float,float,float,int,float,float,int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int))instead.*

Create a new MotionEvent, filling in all of the basic values that define the motion.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when the user originally pressed down to start a stream of position events. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when this specific event was generated. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The kind of action being performed, such as [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int). |
| `pointerCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of pointers that are active in this event. |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of this event. |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of this event. |
| `pressure` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The current pressure of this event. The pressure generally ranges from 0 (no pressure at all) to 1 (normal pressure), however values higher than 1 may be generated depending on the calibration of the input device. |
| `size` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A scaled value of the approximate size of the area being pressed when touched with the finger. The actual value in pixels corresponding to the finger touch is normalized with a device specific range of values and scaled to a value between 0 and 1. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The state of any meta / modifier keys that were in effect when the event was generated. |
| `xPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the X coordinate being reported. |
| `yPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the Y coordinate being reported. |
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID for the device that this event came from. An ID of zero indicates that the event didn't come from a physical device; other numbers are arbitrary and you shouldn't depend on the values. |
| `edgeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitfield indicating which edges, if any, were touched by this MotionEvent. |

### obtain

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(
    downTime: Long, 
    eventTime: Long, 
    action: Int, 
    pointerCount: Int, 
    pointerIds: IntArray!, 
    pointerCoords: Array<MotionEvent.PointerCoords!>!, 
    metaState: Int, 
    xPrecision: Float, 
    yPrecision: Float, 
    deviceId: Int, 
    edgeFlags: Int, 
    source: Int, 
    flags: Int
): MotionEvent!
```

**Deprecated:** *Use[obtain(long,long,int,int,android.view.MotionEvent.PointerProperties[],android.view.MotionEvent.PointerCoords[],int,int,float,float,int,int,int,int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array,%20kotlin.Array,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))instead.*

Create a new MotionEvent, filling in all of the basic values that define the motion.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `downTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when the user originally pressed down to start a stream of position events. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time (in ms) when this specific event was generated. This must be obtained from [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()). |
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The kind of action being performed, such as [ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/MotionEvent#ACTION_DOWN:kotlin.Int). |
| `pointerCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of pointers that will be in this event. |
| `pointerIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:An array of*pointerCount*values providing an identifier for each pointer. |
| `pointerCoords` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MotionEvent.PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords)!\>!:An array of*pointerCount* values providing a [PointerCoords](https://developer.android.com/reference/kotlin/android/view/MotionEvent.PointerCoords) coordinate object for each pointer. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The state of any meta / modifier keys that were in effect when the event was generated. |
| `xPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the X coordinate being reported. |
| `yPrecision` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The precision of the Y coordinate being reported. |
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID for the device that this event came from. An ID of zero indicates that the event didn't come from a physical device; other numbers are arbitrary and you shouldn't depend on the values. |
| `edgeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitfield indicating which edges, if any, were touched by this MotionEvent. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The source of this event. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The motion event flags. |

### obtainNoHistory

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtainNoHistory(other: MotionEvent!): MotionEvent!
```

Create a new MotionEvent, copying from an existing one, but not including any historical point information. 

### offsetLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun offsetLocation(
    deltaX: Float, 
    deltaY: Float
): Unit
```

Adjust this event's location.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `deltaX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Amount to add to the current X coordinate of the event. |
| `deltaY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Amount to add to the current Y coordinate of the event. |

### recycle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun recycle(): Unit
```

Recycle the MotionEvent, to be re-used by a later caller. After calling this function you must not ever touch the event again. 

### setAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAction(action: Int): Unit
```

Sets this event's action. 

### setEdgeFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setEdgeFlags(flags: Int): Unit
```

Sets the bitfield indicating which edges, if any, were touched by this MotionEvent. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/view/MotionEvent#getEdgeFlags()> 

### setLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLocation(
    x: Float, 
    y: Float
): Unit
```

Set this event's location. Applies [offsetLocation](https://developer.android.com/reference/kotlin/android/view/MotionEvent#offsetLocation(kotlin.Float,%20kotlin.Float))with a delta from the current location to the given new location.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):New absolute X location. |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):New absolute Y location. |

### setSource

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSource(source: Int): Unit
```  

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### transform

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun transform(matrix: Matrix!): Unit
```

Applies a transformation matrix to all of the points in the event.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `matrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)!:The transformation matrix to apply. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<MotionEvent!>
```
