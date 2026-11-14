# CountedCompleter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CountedCompleter

```
abstract class CountedCompleter<T : Any!> : ForkJoinTask<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.concurrent.ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)\<T\> ||
| | ↳ | [java.util.concurrent.CountedCompleter](../java/util/concurrent/CountedCompleter.md) |

A [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md) with a completion action performed when triggered and there are no remaining pending actions. CountedCompleters are in general more robust in the presence of subtask stalls and blockage than are other forms of ForkJoinTasks, but are less intuitive to program. Uses of CountedCompleter are similar to those of other completion based components (such as [java.nio.channels.CompletionHandler](../java/nio/channels/CompletionHandler.md)) except that multiple*pending* completions may be necessary to trigger the completion action , not just one. Unless initialized otherwise, the [pending](../java/util/concurrent/CountedCompleter.md))starts at zero, but may be (atomically) changed using methods [setPendingCount](../java/util/concurrent/CountedCompleter.md)), [addToPendingCount](../java/util/concurrent/CountedCompleter.md)), and [compareAndSetPendingCount](../java/util/concurrent/CountedCompleter.md)). Upon invocation of [tryComplete](../java/util/concurrent/CountedCompleter.md)), if the pending action count is nonzero, it is decremented; otherwise, the completion action is performed, and if this completer itself has a completer, the process is continued with its completer. As is the case with related synchronization components such as [Phaser](../java/util/concurrent/Phaser.md) and [Semaphore](../java/util/concurrent/Semaphore.md), these methods affect only internal counts; they do not establish any further internal bookkeeping. In particular, the identities of pending tasks are not maintained. As illustrated below, you can create subclasses that do record some or all pending tasks or their results when needed. As illustrated below, utility methods supporting customization of completion traversals are also provided. However, because CountedCompleters provide only basic synchronization mechanisms, it may be useful to create further abstract subclasses that maintain linkages, fields, and additional support methods appropriate for a set of related usages.

A concrete CountedCompleter class must define method [compute](../java/util/concurrent/CountedCompleter.md)), that should in most cases (as illustrated below), invoke`tryComplete()`once before returning. The class may also optionally override method [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md))to perform an action upon normal completion, and method [onExceptionalCompletion(java.lang.Throwable,java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md))to perform an action upon any exception.

CountedCompleters most often do not bear results, in which case they are normally declared as`CountedCompleter<Void>`, and will always return`null`as a result value. In other cases, you should override method [getRawResult](../java/util/concurrent/CountedCompleter.md))to provide a result from`join(), invoke()`, and related methods. In general, this method should return the value of a field (or a function of one or more fields) of the CountedCompleter object that holds the result upon completion. Method [setRawResult](../java/util/concurrent/CountedCompleter.md))by default plays no role in CountedCompleters. It is possible, but rarely applicable, to override this method to maintain other objects or fields holding result data.

A CountedCompleter that does not itself have a completer (i.e., one for which [getCompleter](../java/util/concurrent/CountedCompleter.md))returns`null`) can be used as a regular ForkJoinTask with this added functionality. However, any completer that in turn has another completer serves only as an internal helper for other computations, so its own task status (as reported in methods such as [ForkJoinTask.isDone](../java/util/concurrent/ForkJoinTask.md))) is arbitrary; this status changes only upon explicit invocations of [complete](../java/util/concurrent/CountedCompleter.md)), [ForkJoinTask.cancel](../java/util/concurrent/ForkJoinTask.md)), [ForkJoinTask.completeExceptionally(Throwable)](../java/util/concurrent/ForkJoinTask.md))or upon exceptional completion of method`compute`. Upon any exceptional completion, the exception may be relayed to a task's completer (and its completer, and so on), if one exists and it has not otherwise already completed. Similarly, cancelling an internal CountedCompleter has only a local effect on that completer, so is not often useful.

**Sample Usages.**

**Parallel recursive decomposition.** CountedCompleters may be arranged in trees similar to those often used with [RecursiveAction](../java/util/concurrent/RecursiveAction.md) s, although the constructions involved in setting them up typically vary. Here, the completer of each task is its parent in the computation tree. Even though they entail a bit more bookkeeping, CountedCompleters may be better choices when applying a possibly time-consuming operation (that cannot be further subdivided) to each element of an array or collection; especially when the operation takes a significantly different amount of time to complete for some elements than others, either because of intrinsic variation (for example I/O) or auxiliary effects such as garbage collection. Because CountedCompleters provide their own continuations, other tasks need not block waiting to perform them.

For example, here is an initial version of a utility method that uses divide-by-two recursive decomposition to divide work into single pieces (leaf tasks). Even when work is split into individual calls, tree-based techniques are usually preferable to directly forking leaf tasks, because they reduce inter-thread communication and improve load balancing. In the recursive case, the second of each pair of subtasks to finish triggers completion of their parent (because no result combination is performed, the default no-op implementation of method`onCompletion`is not overridden). The utility method sets up the root task and invokes it (here, implicitly using the [ForkJoinPool.commonPool()](../java/util/concurrent/ForkJoinPool.md))). It is straightforward and reliable (but not optimal) to always set the pending count to the number of child tasks and call`tryComplete()`immediately before returning. 

```kotlin
<code>public static &lt;E&gt; void forEach(E[] array, Consumer&lt;E&gt; action) {
    class Task extends CountedCompleter&lt;Void&gt; {
      final int lo, hi;
      Task(Task parent, int lo, int hi) {
        super(parent); this.lo = lo; this.hi = hi;
      }
 
      public void compute() {
        if (hi - lo &gt;= 2) {
          int mid = (lo + hi) &gt;&gt;&gt; 1;
          // must set pending count before fork
          setPendingCount(2);
          new Task(this, mid, hi).fork(); // right child
          new Task(this, lo, mid).fork(); // left child
        }
        else if (hi &gt; lo)
          action.accept(array[lo]);
        tryComplete();
      }
    }
    new Task(null, 0, array.length).invoke();
  }</code>
```
This design can be improved by noticing that in the recursive case, the task has nothing to do after forking its right task, so can directly invoke its left task before returning. (This is an analog of tail recursion removal.) Also, when the last action in a task is to fork or invoke a subtask (a "tail call"), the call to`tryComplete()`can be optimized away, at the cost of making the pending count look "off by one". 

```kotlin
<code>public void compute() {
        if (hi - lo &gt;= 2) {
          int mid = (lo + hi) &gt;&gt;&gt; 1;
          setPendingCount(1); // looks off by one, but correct!
          new Task(this, mid, hi).fork(); // right child
          new Task(this, lo, mid).compute(); // direct invoke
        } else {
          if (hi &gt; lo)
            action.accept(array[lo]);
          tryComplete();
        }
      }</code>
```
As a further optimization, notice that the left task need not even exist. Instead of creating a new one, we can continue using the original task, and add a pending count for each fork. Additionally, because no task in this tree implements an [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md))method,`tryComplete`can be replaced with [propagateCompletion](../java/util/concurrent/CountedCompleter.md)). 

```kotlin
<code>public void compute() {
        int n = hi - lo;
        for (; n &gt;= 2; n /= 2) {
          addToPendingCount(1);
          new Task(this, lo + n/2, lo + n).fork();
        }
        if (n &gt; 0)
          action.accept(array[lo]);
        propagateCompletion();
      }</code>
```
When pending counts can be precomputed, they can be established in the constructor: 

```kotlin
<code>public static &lt;E&gt; void forEach(E[] array, Consumer&lt;E&gt; action) {
    class Task extends CountedCompleter&lt;Void&gt; {
      final int lo, hi;
      Task(Task parent, int lo, int hi) {
        super(parent, 31 - Integer.numberOfLeadingZeros(hi - lo));
        this.lo = lo; this.hi = hi;
      }
 
      public void compute() {
        for (int n = hi - lo; n &gt;= 2; n /= 2)
          new Task(this, lo + n/2, lo + n).fork();
        action.accept(array[lo]);
        propagateCompletion();
      }
    }
    if (array.length &gt; 0)
      new Task(null, 0, array.length).invoke();
  }</code>
```
Additional optimizations of such classes might entail specializing classes for leaf steps, subdividing by say, four, instead of two per iteration, and using an adaptive threshold instead of always subdividing down to single elements.

**Searching.** A tree of CountedCompleters can search for a value or property in different parts of a data structure, and report a result in an as soon as one is found. The others can poll the result to avoid unnecessary work. (You could additionally [cancel](../java/util/concurrent/ForkJoinTask.md))other tasks, but it is usually simpler and more efficient to just let them notice that the result is set and if so skip further processing.) Illustrating again with an array using full partitioning (again, in practice, leaf tasks will almost always process more than one element): 

```kotlin
<code>class Searcher&lt;E&gt; extends CountedCompleter&lt;E&gt; {
    final E[] array; final AtomicReference&lt;E&gt; result; final int lo, hi;
    Searcher(CountedCompleter&lt;?&gt; p, E[] array, AtomicReference&lt;E&gt; result, int lo, int hi) {
      super(p);
      this.array = array; this.result = result; this.lo = lo; this.hi = hi;
    }
    public E getRawResult() { return result.get(); }
    public void compute() { // similar to ForEach version 3
      int l = lo, h = hi;
      while (result.get() == null &amp;&amp; h &gt;= l) {
        if (h - l &gt;= 2) {
          int mid = (l + h) &gt;&gt;&gt; 1;
          addToPendingCount(1);
          new Searcher(this, array, result, mid, h).fork();
          h = mid;
        }
        else {
          E x = array[l];
          if (matches(x) &amp;&amp; result.compareAndSet(null, x))
            quietlyCompleteRoot(); // root task is now joinable
          break;
        }
      }
      tryComplete(); // normally complete whether or not found
    }
    boolean matches(E e) { ... } // return true if found
 
    public static &lt;E&gt; E search(E[] array) {
        return new Searcher&lt;E&gt;(null, array, new AtomicReference&lt;E&gt;(), 0, array.length).invoke();
    }
  }</code>
```
In this example, as well as others in which tasks have no other effects except to`compareAndSet`a common result, the trailing unconditional invocation of`tryComplete`could be made conditional (`if (result.get() == null) tryComplete();`) because no further bookkeeping is required to manage completions once the root task completes.

**Recording subtasks.** CountedCompleter tasks that combine results of multiple subtasks usually need to access these results in method [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md)). As illustrated in the following class (that performs a simplified form of map-reduce where mappings and reductions are all of type`E`), one way to do this in divide and conquer designs is to have each subtask record its sibling, so that it can be accessed in method`onCompletion`. This technique applies to reductions in which the order of combining left and right results does not matter; ordered reductions require explicit left/right designations. Variants of other streamlinings seen in the above examples may also apply. 

```kotlin
<code>class MyMapper&lt;E&gt; { E apply(E v) {  ...  } }
  class MyReducer&lt;E&gt; { E apply(E x, E y) {  ...  } }
  class MapReducer&lt;E&gt; extends CountedCompleter&lt;E&gt; {
    final E[] array; final MyMapper&lt;E&gt; mapper;
    final MyReducer&lt;E&gt; reducer; final int lo, hi;
    MapReducer&lt;E&gt; sibling;
    E result;
    MapReducer(CountedCompleter&lt;?&gt; p, E[] array, MyMapper&lt;E&gt; mapper,
               MyReducer&lt;E&gt; reducer, int lo, int hi) {
      super(p);
      this.array = array; this.mapper = mapper;
      this.reducer = reducer; this.lo = lo; this.hi = hi;
    }
    public void compute() {
      if (hi - lo &gt;= 2) {
        int mid = (lo + hi) &gt;&gt;&gt; 1;
        MapReducer&lt;E&gt; left = new MapReducer(this, array, mapper, reducer, lo, mid);
        MapReducer&lt;E&gt; right = new MapReducer(this, array, mapper, reducer, mid, hi);
        left.sibling = right;
        right.sibling = left;
        setPendingCount(1); // only right is pending
        right.fork();
        left.compute();     // directly execute left
      }
      else {
        if (hi &gt; lo)
            result = mapper.apply(array[lo]);
        tryComplete();
      }
    }
    public void onCompletion(CountedCompleter&lt;?&gt; caller) {
      if (caller != this) {
        MapReducer&lt;E&gt; child = (MapReducer&lt;E&gt;)caller;
        MapReducer&lt;E&gt; sib = child.sibling;
        if (sib == null || sib.result == null)
          result = child.result;
        else
          result = reducer.apply(child.result, sib.result);
      }
    }
    public E getRawResult() { return result; }
 
    public static &lt;E&gt; E mapReduce(E[] array, MyMapper&lt;E&gt; mapper, MyReducer&lt;E&gt; reducer) {
      return new MapReducer&lt;E&gt;(null, array, mapper, reducer,
                               0, array.length).invoke();
    }
  }</code>
```
Here, method`onCompletion`takes a form common to many completion designs that combine results. This callback-style method is triggered once per task, in either of the two different contexts in which the pending count is, or becomes, zero: (1) by a task itself, if its pending count is zero upon invocation of`tryComplete`, or (2) by any of its subtasks when they complete and decrement the pending count to zero. The`caller`argument distinguishes cases. Most often, when the caller is`this`, no action is necessary. Otherwise the caller argument can be used (usually via a cast) to supply a value (and/or links to other values) to be combined. Assuming proper use of pending counts, the actions inside`onCompletion`occur (once) upon completion of a task and its subtasks. No additional synchronization is required within this method to ensure thread safety of accesses to fields of this task or other completed tasks.

**Completion Traversals.** If using`onCompletion`to process completions is inapplicable or inconvenient, you can use methods [firstComplete](../java/util/concurrent/CountedCompleter.md))and [nextComplete](../java/util/concurrent/CountedCompleter.md))to create custom traversals. For example, to define a MapReducer that only splits out right-hand tasks in the form of the third ForEach example, the completions must cooperatively reduce along unexhausted subtask links, which can be done as follows: 

```kotlin
<code>class MapReducer&lt;E&gt; extends CountedCompleter&lt;E&gt; { // version 2
    final E[] array; final MyMapper&lt;E&gt; mapper;
    final MyReducer&lt;E&gt; reducer; final int lo, hi;
    MapReducer&lt;E&gt; forks, next; // record subtask forks in list
    E result;
    MapReducer(CountedCompleter&lt;?&gt; p, E[] array, MyMapper&lt;E&gt; mapper,
               MyReducer&lt;E&gt; reducer, int lo, int hi, MapReducer&lt;E&gt; next) {
      super(p);
      this.array = array; this.mapper = mapper;
      this.reducer = reducer; this.lo = lo; this.hi = hi;
      this.next = next;
    }
    public void compute() {
      int l = lo, h = hi;
      while (h - l &gt;= 2) {
        int mid = (l + h) &gt;&gt;&gt; 1;
        addToPendingCount(1);
        (forks = new MapReducer(this, array, mapper, reducer, mid, h, forks)).fork();
        h = mid;
      }
      if (h &gt; l)
        result = mapper.apply(array[l]);
      // process completions by reducing along and advancing subtask links
      for (CountedCompleter&lt;?&gt; c = firstComplete(); c != null; c = c.nextComplete()) {
        for (MapReducer t = (MapReducer)c, s = t.forks; s != null; s = t.forks = s.next)
          t.result = reducer.apply(t.result, s.result);
      }
    }
    public E getRawResult() { return result; }
 
    public static &lt;E&gt; E mapReduce(E[] array, MyMapper&lt;E&gt; mapper, MyReducer&lt;E&gt; reducer) {
      return new MapReducer&lt;E&gt;(null, array, mapper, reducer,
                               0, array.length, null).invoke();
    }
  }</code>
```

**Triggers.**Some CountedCompleters are themselves never forked, but instead serve as bits of plumbing in other designs; including those in which the completion of one or more async tasks triggers another async task. For example: 

```kotlin
<code>class HeaderBuilder extends CountedCompleter&lt;...&gt; { ... }
  class BodyBuilder extends CountedCompleter&lt;...&gt; { ... }
  class PacketSender extends CountedCompleter&lt;...&gt; {
    PacketSender(...) { super(null, 1); ... } // trigger on second completion
    public void compute() { } // never called
    public void onCompletion(CountedCompleter&lt;?&gt; caller) { sendPacket(); }
  }
  // sample use:
  PacketSender p = new PacketSender();
  new HeaderBuilder(p, ...).fork();
  new BodyBuilder(p, ...).fork();</code>
```

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md))`()` Creates a new CountedCompleter with no completer and an initial pending count of zero. |
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md))`(`completer:` ` [CountedCompleter](../java/util/concurrent/CountedCompleter.md)<*>!`)` Creates a new CountedCompleter with the given completer and an initial pending count of zero. |
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md))`(`completer:` ` [CountedCompleter](../java/util/concurrent/CountedCompleter.md)<*>!`, `initialPendingCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new CountedCompleter with the given completer and initial pending count. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addToPendingCount](../java/util/concurrent/CountedCompleter.md))`(`delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds (atomically) the given value to the pending count. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSetPendingCount](../java/util/concurrent/CountedCompleter.md))`(`expected:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets (atomically) the pending count to the given count only if it currently holds the given expected value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [complete](../java/util/concurrent/CountedCompleter.md))`(`rawResult:` `T`)` Regardless of pending count, invokes [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md)), marks this task as complete and further triggers [tryComplete](../java/util/concurrent/CountedCompleter.md))on this task's completer, if one exists. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [compute](../java/util/concurrent/CountedCompleter.md))`()` The main computation performed by this task. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [decrementPendingCountUnlessZero](../java/util/concurrent/CountedCompleter.md))`()` If the pending count is nonzero, (atomically) decrements it. |
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md)\<\*\>! | [firstComplete](../java/util/concurrent/CountedCompleter.md))`()` If this task's pending count is zero, returns this task; otherwise decrements its pending count and returns`null`. |
| --- | --- |
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md)\<\*\>! | [getCompleter](../java/util/concurrent/CountedCompleter.md))`()` Returns the completer established in this task's constructor, or`null`if none. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPendingCount](../java/util/concurrent/CountedCompleter.md))`()` Returns the current pending count. |
| openT | [getRawResult](../java/util/concurrent/CountedCompleter.md))`()` Returns the result of the computation. |
| --- | --- |
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md)\<\*\>! | [getRoot](../java/util/concurrent/CountedCompleter.md))`()` Returns the root of the current computation; i. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [helpComplete](../java/util/concurrent/CountedCompleter.md))`(`maxTasks:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` If this task has not completed, attempts to process at most the given number of other unprocessed tasks for which this task is on the completion path, if any are known to exist. |
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md)\<\*\>! | [nextComplete](../java/util/concurrent/CountedCompleter.md))`()` If this task does not have a completer, invokes [java.util.concurrent.ForkJoinTask#quietlyComplete](../java/util/concurrent/ForkJoinTask.md))and returns`null`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCompletion](../java/util/concurrent/CountedCompleter.md))`(`caller:` ` [CountedCompleter](../java/util/concurrent/CountedCompleter.md)<*>!`)` Performs an action when method [tryComplete](../java/util/concurrent/CountedCompleter.md))is invoked and the pending count is zero, or when the unconditional method [complete](../java/util/concurrent/CountedCompleter.md))is invoked. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onExceptionalCompletion](../java/util/concurrent/CountedCompleter.md))`(`ex:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`, `caller:` ` [CountedCompleter](../java/util/concurrent/CountedCompleter.md)<*>!`)` Performs an action when method [completeExceptionally(java.lang.Throwable)](../java/util/concurrent/ForkJoinTask.md))is invoked or method [compute](../java/util/concurrent/CountedCompleter.md))throws an exception, and this task has not already otherwise completed normally. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [propagateCompletion](../java/util/concurrent/CountedCompleter.md))`()` Equivalent to [tryComplete](../java/util/concurrent/CountedCompleter.md))but does not invoke [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md))along the completion path: If the pending count is nonzero, decrements the count; otherwise, similarly tries to complete this task's completer, if one exists, else marks this task as complete. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quietlyCompleteRoot](../java/util/concurrent/CountedCompleter.md))`()` Equivalent to`getRoot().quietlyComplete()`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPendingCount](../java/util/concurrent/CountedCompleter.md))`(`count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the pending count to the given value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tryComplete](../java/util/concurrent/CountedCompleter.md))`()` If the pending count is nonzero, decrements the count; otherwise invokes [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md))and then similarly tries to complete this task's completer, if one exists, else marks this task as complete. |
| --- | --- |

| Protected methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [exec](../java/util/concurrent/CountedCompleter.md))`()` Implements execution conventions for CountedCompleters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRawResult](../java/util/concurrent/CountedCompleter.md))`(`t:` `T`)` A method that result-bearing CountedCompleters may optionally use to help maintain result data. |

| Inherited functions ||
|---|---|
| From class [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md) |-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<*>! | [adapt](../java/util/concurrent/ForkJoinTask.md))`(`runnable:` ` [Runnable](../java/lang/Runnable.md)!`)` <br /> Returns a new`ForkJoinTask`that performs the`run`method of the given`Runnable`as its action, and returns a null result upon [join](../java/util/concurrent/ForkJoinTask.md)). <br /> | | [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<T>! | [adapt](../java/util/concurrent/ForkJoinTask.md))`(`runnable:` ` [Runnable](../java/lang/Runnable.md)!`, `result:` `T`)` <br /> Returns a new`ForkJoinTask`that performs the`run`method of the given`Runnable`as its action, and returns the given result upon [join](../java/util/concurrent/ForkJoinTask.md)). <br /> | | [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<T>! | [adapt](../java/util/concurrent/ForkJoinTask.md))`(`callable:` ` [Callable](../java/util/concurrent/Callable.md)<out` `T>!`)` <br /> Returns a new`ForkJoinTask`that performs the`call`method of the given`Callable`as its action, and returns its result upon [join](../java/util/concurrent/ForkJoinTask.md)), translating any checked exceptions encountered into`RuntimeException`. <br /> | | [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<T>! | [adaptInterruptible](../java/util/concurrent/ForkJoinTask.md))`(`callable:` ` [Callable](../java/util/concurrent/Callable.md)<out` `T>!`)` <br /> Returns a new`ForkJoinTask`that performs the`call`method of the given`Callable`as its action, and returns its result upon [join](../java/util/concurrent/ForkJoinTask.md)), translating any checked exceptions encountered into`RuntimeException`. Additionally, invocations of`cancel`with`mayInterruptIfRunning true`will attempt to interrupt the thread performing the task. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](../java/util/concurrent/ForkJoinTask.md))`(`mayInterruptIfRunning:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to cancel execution of this task. This attempt will fail if the task has already completed or could not be cancelled for some other reason. If successful, and this task has not started when`cancel`is called, execution of this task is suppressed. After this method returns successfully, unless there is an intervening call to [reinitialize](../java/util/concurrent/ForkJoinTask.md)), subsequent calls to [isCancelled](../java/util/concurrent/ForkJoinTask.md)), [isDone](../java/util/concurrent/ForkJoinTask.md)), and`cancel`will return`true`and calls to [join](../java/util/concurrent/ForkJoinTask.md))and related methods will result in`CancellationException`. This method may be overridden in subclasses, but if so, must still ensure that these properties hold. In particular, the`cancel`method itself must not throw exceptions. This method is designed to be invoked by*other* tasks. To terminate the current task, you can just return or throw an unchecked exception from its computation method, or invoke [completeExceptionally(java.lang.Throwable)](../java/util/concurrent/ForkJoinTask.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSetForkJoinTaskTag](../java/util/concurrent/ForkJoinTask.md))`(`expect:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `update:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> Atomically conditionally sets the tag value for this task. Among other applications, tags can be used as visit markers in tasks operating on graphs, as in methods that check:`if (task.compareAndSetForkJoinTaskTag((short)0, (short)1))`before processing, otherwise exiting because the node has already been visited. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [completeExceptionally](../java/util/concurrent/ForkJoinTask.md))`(`ex:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> Completes this task abnormally, and if not already aborted or cancelled, causes it to throw the given exception upon`join`and related operations. This method may be used to induce exceptions in asynchronous tasks, or to force completion of tasks that would not otherwise complete. Its use in other situations is discouraged. This method is overridable, but overridden versions must invoke`super`implementation to maintain guarantees. <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [exceptionNow](../java/util/concurrent/ForkJoinTask.md))`()` <br /> | | [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<V>! | [fork](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Arranges to asynchronously execute this task in the pool the current task is running in, if applicable, or using the [java.util.concurrent.ForkJoinPool#commonPool()](../java/util/concurrent/ForkJoinPool.md))if not [inForkJoinPool](../java/util/concurrent/ForkJoinTask.md)). While it is not necessarily enforced, it is a usage error to fork a task more than once unless it has completed and been reinitialized. Subsequent modifications to the state of this task or any data it operates on are not necessarily consistently observable by any thread other than the one executing it unless preceded by a call to [join](../java/util/concurrent/ForkJoinTask.md))or related methods, or a call to [isDone](../java/util/concurrent/ForkJoinTask.md))returning`true`. <br /> | | V | [get](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Waits if necessary for the computation to complete, and then retrieves its result. <br /> | | V | [get](../java/util/concurrent/ForkJoinTask.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` <br /> Waits if necessary for at most the given time for the computation to complete, and then retrieves its result, if available. <br /> | | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getException](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns the exception thrown by the base computation, or a`CancellationException`if cancelled, or`null`if none or if the method has not yet completed. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getForkJoinTaskTag](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns the tag for this task. <br /> | | [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md)! | [getPool](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns the pool hosting the current thread, or`null`if the current thread is executing outside of any ForkJoinPool. This method returns`null`if and only if [inForkJoinPool](../java/util/concurrent/ForkJoinTask.md))returns`false`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQueuedTaskCount](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns an estimate of the number of tasks that have been forked by the current worker thread but not yet executed. This value may be useful for heuristic decisions about whether to fork other tasks. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSurplusQueuedTaskCount](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns an estimate of how many more locally queued tasks are held by the current worker thread than there are other worker threads that might steal them, or zero if this thread is not operating in a ForkJoinPool. This value may be useful for heuristic decisions about whether to fork other tasks. In many usages of ForkJoinTasks, at steady state, each worker should aim to maintain a small constant surplus (for example, 3) of tasks, and to process computations locally if this threshold is exceeded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [helpQuiesce](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Possibly executes tasks until the pool hosting the current task [is quiescent](../java/util/concurrent/ForkJoinPool.md)). This method may be of use in designs in which many tasks are forked, but none are explicitly joined, instead executing them until all are processed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inForkJoinPool](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns`true`if the current thread is a [ForkJoinWorkerThread](../java/util/concurrent/ForkJoinWorkerThread.md) executing as a ForkJoinPool computation. <br /> | | V | [invoke](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Commences performing this task, awaits its completion if necessary, and returns its result, or throws an (unchecked)`RuntimeException`or`Error`if the underlying computation did so. <br /> | | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<T>! | [invokeAll](../java/util/concurrent/ForkJoinTask.md))`(`tasks:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<T>!`)` <br /> Forks all tasks in the specified collection, returning when`isDone`holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, others may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using [getException()](../java/util/concurrent/ForkJoinTask.md))and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invokeAll](../java/util/concurrent/ForkJoinTask.md))`(`t1:` ` [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<*>!`, `t2:` ` [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<*>!`)` <br /> Forks the given tasks, returning when`isDone`holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, the other may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using [getException()](../java/util/concurrent/ForkJoinTask.md))and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invokeAll](../java/util/concurrent/ForkJoinTask.md))`(`vararg` `tasks:` ` [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<*>!`)` <br /> Forks the given tasks, returning when`isDone`holds for each task or an (unchecked) exception is encountered, in which case the exception is rethrown. If more than one task encounters an exception, then this method throws any one of these exceptions. If any task encounters an exception, others may be cancelled. However, the execution status of individual tasks is not guaranteed upon exceptional return. The status of each task may be obtained using [getException()](../java/util/concurrent/ForkJoinTask.md))and related methods to check if they have been cancelled, completed normally or exceptionally, or left unprocessed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](../java/util/concurrent/ForkJoinTask.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCompletedAbnormally](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns`true`if this task threw an exception or was cancelled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCompletedNormally](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns`true`if this task completed without throwing an exception and was not cancelled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](../java/util/concurrent/ForkJoinTask.md))`()` <br /> | | V | [join](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns the result of the computation when it [is done](../java/util/concurrent/ForkJoinTask.md)). This method differs from [get()](../java/util/concurrent/ForkJoinTask.md))in that abnormal completion results in`RuntimeException`or`Error`, not`ExecutionException`, and that interrupts of the calling thread do*not* cause the method to abruptly return by throwing`InterruptedException`. <br /> | | [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<*>! | [peekNextLocalTask](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Returns, but does not unschedule or execute, a task queued by the current thread but not yet executed, if one is immediately available. There is no guarantee that this task will actually be polled or executed next. Conversely, this method may return null even if a task exists but cannot be accessed without contention with other threads. This method is designed primarily to support extensions, and is unlikely to be useful otherwise. <br /> | | [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<*>! | [pollNextLocalTask](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if the current thread is operating in a ForkJoinPool. This method is designed primarily to support extensions, and is unlikely to be useful otherwise. <br /> | | [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)<*>! | [pollTask](../java/util/concurrent/ForkJoinTask.md))`()` <br /> If the current thread is operating in a ForkJoinPool, unschedules and returns, without executing, the next task queued by the current thread but not yet executed, if one is available, or if not available, a task that was forked by some other thread, if available. Availability may be transient, so a`null`result does not necessarily imply quiescence of the pool this task is operating in. This method is designed primarily to support extensions, and is unlikely to be useful otherwise. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quietlyComplete](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Completes this task normally without setting a value. The most recent value established by [setRawResult](../java/util/concurrent/ForkJoinTask.md))(or`null`by default) will be returned as the result of subsequent invocations of`join`and related operations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quietlyInvoke](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Commences performing this task and awaits its completion if necessary, without returning its result or throwing its exception. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [quietlyJoin](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Joins this task, without returning its result or throwing its exception. This method may be useful when processing collections of tasks when some have been cancelled or otherwise known to have aborted. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quietlyJoin](../java/util/concurrent/ForkJoinTask.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` <br /> Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout and the current thread has not been interrupted. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quietlyJoinUninterruptibly](../java/util/concurrent/ForkJoinTask.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` <br /> Tries to join this task, returning true if it completed (possibly exceptionally) before the given timeout. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reinitialize](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Resets the internal bookkeeping state of this task, allowing a subsequent`fork`. This method allows repeated reuse of this task, but only if reuse occurs when this task has either never been forked, or has been forked, then completed and all outstanding joins of this task have also completed. Effects under any other usage conditions are not guaranteed. This method may be useful when executing pre-constructed trees of subtasks in loops. Upon completion of this method,`isDone()`reports`false`, and`getException()`reports`null`. However, the value returned by`getRawResult`is unaffected. To clear this value, you can invoke`setRawResult(null)`. <br /> | | V | [resultNow](../java/util/concurrent/ForkJoinTask.md))`()` <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [setForkJoinTaskTag](../java/util/concurrent/ForkJoinTask.md))`(`newValue:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> Atomically sets the tag value for this task and returns the old value. <br /> | | [Future.State](../java/util/concurrent/Future.State.md)! | [state](../java/util/concurrent/ForkJoinTask.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryUnfork](../java/util/concurrent/ForkJoinTask.md))`()` <br /> Tries to unschedule this task for execution. This method will typically (but is not guaranteed to) succeed if this task is the most recently forked task by the current thread, and has not commenced executing in another thread. This method may be useful when arranging alternative local processing of tasks that could have been, but were not, stolen. <br /> | ||

## Protected constructors

### CountedCompleter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CountedCompleter()
```

Creates a new CountedCompleter with no completer and an initial pending count of zero. 

### CountedCompleter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CountedCompleter(completer: CountedCompleter<*>!)
```

Creates a new CountedCompleter with the given completer and an initial pending count of zero.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `completer` | [CountedCompleter](../java/util/concurrent/CountedCompleter.md)\<\*\>!:this task's completer, or`null`if none |

### CountedCompleter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CountedCompleter(
    completer: CountedCompleter<*>!, 
    initialPendingCount: Int)
```

Creates a new CountedCompleter with the given completer and initial pending count.

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `completer` | [CountedCompleter](../java/util/concurrent/CountedCompleter.md)\<\*\>!:this task's completer, or`null`if none |
| `initialPendingCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial pending count |

## Public methods

### addToPendingCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addToPendingCount(delta: Int): Unit
```

Adds (atomically) the given value to the pending count.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `delta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to add |

### compareAndSetPendingCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndSetPendingCount(
    expected: Int, 
    count: Int
): Boolean
```

Sets (atomically) the pending count to the given count only if it currently holds the given expected value.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------|
| `expected` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### complete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun complete(rawResult: T): Unit
```

Regardless of pending count, invokes [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md)), marks this task as complete and further triggers [tryComplete](../java/util/concurrent/CountedCompleter.md))on this task's completer, if one exists. The given rawResult is used as an argument to [setRawResult](../java/util/concurrent/CountedCompleter.md))before invoking [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md))or marking this task as complete; its value is meaningful only for classes overriding`setRawResult`. This method does not modify the pending count.

This method may be useful when forcing completion as soon as any one (versus all) of several subtask results are obtained. However, in the common (and recommended) case in which`setRawResult`is not overridden, this effect can be obtained more simply using [quietlyCompleteRoot()](../java/util/concurrent/CountedCompleter.md)).

| Parameters ||
|-------------|--------------------------------|
| `value` | the result value for this task |
| `rawResult` | T:the raw result |

### compute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compute(): Unit
```

The main computation performed by this task. 

### decrementPendingCountUnlessZero

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun decrementPendingCountUnlessZero(): Int
```

If the pending count is nonzero, (atomically) decrements it.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the initial (undecremented) pending count holding on entry to this method |

### firstComplete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun firstComplete(): CountedCompleter<*>!
```

If this task's pending count is zero, returns this task; otherwise decrements its pending count and returns`null`. This method is designed to be used with [nextComplete](../java/util/concurrent/CountedCompleter.md))in completion traversal loops.

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md)<*>! | this task, if pending count was zero, else`null` |

### getCompleter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCompleter(): CountedCompleter<*>!
```

Returns the completer established in this task's constructor, or`null`if none.

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------|
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md)<*>! | the completer |

### getPendingCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPendingCount(): Int
```

Returns the current pending count.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current pending count |

### getRawResult

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRawResult(): T
```

Returns the result of the computation. By default, returns`null`, which is appropriate for`Void`actions, but in other cases should be overridden, almost always to return a field or function of a field that holds the result upon completion.

| Return ||
|---|-------------------------------|
| T | the result of the computation |

### getRoot

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoot(): CountedCompleter<*>!
```

Returns the root of the current computation; i.e., this task if it has no completer, else its completer's root.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md)<*>! | the root of the current computation |

### helpComplete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun helpComplete(maxTasks: Int): Unit
```

If this task has not completed, attempts to process at most the given number of other unprocessed tasks for which this task is on the completion path, if any are known to exist.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `maxTasks` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of tasks to process. If less than or equal to zero, then no tasks are processed. |

### nextComplete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextComplete(): CountedCompleter<*>!
```

If this task does not have a completer, invokes [java.util.concurrent.ForkJoinTask#quietlyComplete](../java/util/concurrent/ForkJoinTask.md))and returns`null`. Or, if the completer's pending count is non-zero, decrements that pending count and returns`null`. Otherwise, returns the completer. This method can be used as part of a completion traversal loop for homogeneous task hierarchies: 

```kotlin
<code>for (CountedCompleter&lt;?&gt; c = firstComplete();
       c != null;
       c = c.nextComplete()) {
    // ... process c ...
  }</code>
```

<br />

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------|
| [CountedCompleter](../java/util/concurrent/CountedCompleter.md)<*>! | the completer, or`null`if none |

### onCompletion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCompletion(caller: CountedCompleter<*>!): Unit
```

Performs an action when method [tryComplete](../java/util/concurrent/CountedCompleter.md))is invoked and the pending count is zero, or when the unconditional method [complete](../java/util/concurrent/CountedCompleter.md))is invoked. By default, this method does nothing. You can distinguish cases by checking the identity of the given caller argument. If not equal to`this`, then it is typically a subtask that may contain results (and/or links to other results) to combine.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `caller` | [CountedCompleter](../java/util/concurrent/CountedCompleter.md)\<\*\>!:the task invoking this method (which may be this task itself) |

### onExceptionalCompletion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onExceptionalCompletion(
    ex: Throwable!, 
    caller: CountedCompleter<*>!
): Boolean
```

Performs an action when method [completeExceptionally(java.lang.Throwable)](../java/util/concurrent/ForkJoinTask.md))is invoked or method [compute](../java/util/concurrent/CountedCompleter.md))throws an exception, and this task has not already otherwise completed normally. On entry to this method, this task [ForkJoinTask.isCompletedAbnormally](../java/util/concurrent/ForkJoinTask.md)). The return value of this method controls further propagation: If`true`and this task has a completer that has not completed, then that completer is also completed exceptionally, with the same exception as this completer. The default implementation of this method does nothing except return`true`.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ex` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the exception |
| `caller` | [CountedCompleter](../java/util/concurrent/CountedCompleter.md)\<\*\>!:the task invoking this method (which may be this task itself) |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this exception should be propagated to this task's completer, if one exists |

### propagateCompletion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun propagateCompletion(): Unit
```

Equivalent to [tryComplete](../java/util/concurrent/CountedCompleter.md))but does not invoke [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md))along the completion path: If the pending count is nonzero, decrements the count; otherwise, similarly tries to complete this task's completer, if one exists, else marks this task as complete. This method may be useful in cases where`onCompletion`should not, or need not, be invoked for each completer in a computation. 

### quietlyCompleteRoot

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun quietlyCompleteRoot(): Unit
```

Equivalent to`getRoot().quietlyComplete()`. 

### setPendingCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPendingCount(count: Int): Unit
```

Sets the pending count to the given value.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the count |

### tryComplete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun tryComplete(): Unit
```

If the pending count is nonzero, decrements the count; otherwise invokes [onCompletion(java.util.concurrent.CountedCompleter)](../java/util/concurrent/CountedCompleter.md))and then similarly tries to complete this task's completer, if one exists, else marks this task as complete.

## Protected methods

### exec

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun exec(): Boolean
```

Implements execution conventions for CountedCompleters.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this task is known to have completed normally |

### setRawResult

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setRawResult(t: T): Unit
```

A method that result-bearing CountedCompleters may optionally use to help maintain result data. By default, does nothing. Overrides are not recommended. However, if this method is overridden to update existing objects or fields, then it must in general be defined to be thread-safe.

| Parameters ||
|---------|-----------|
| `value` | the value |
