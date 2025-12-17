[//]: # (Source: https://www.jetbrains.com/help/idea/debug-kotlin-coroutines.html)
[//]: # (Downloaded: 2025-12-17 19:24:17)

# Debug Kotlin coroutines

While coroutines are particularly well suited for asynchronous programming, there is still room for mistakes, which may be hard to figure out due to the challenges that the asynchronous flow poses.

When debugging Kotlin code, IntelliJ IDEA allows you to suspend the execution and diagnose problems that the code in coroutines may have. The debug information is available even if the coroutine is not running at the moment.

Coroutine debugger provides you with the information on:

  * The list of coroutines and their states grouped by dispatcher. To get the list, go to the Coroutines tab. The top-level nodes are dispatchers, then go coroutines. For each coroutine, you get information on its current state (CREATED, RUNNING, SUSPENDED) and the state of its thread.

![List of coroutines in the Coroutines tab](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin_debug_coroutines_list.png)
  * Coroutine context: the values of local variables and fields available in a coroutine at a certain execution point. When debugging coroutines, you can use all the standard functionality of the Variables tab. For more information about using the Variables tab, refer to the [Examine/update variables](examining-suspended-program.html#variables) topic.

![Variables tab for a coroutine](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin_debug_coroutines_context.png)
  * The coroutine creation stack and the call stack inside the coroutine.

![The coroutine creation stack](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin_debug_coroutines_frames.png)

If you are not interested in calls in Kotlin classes, you can hide them by clicking Hide Frames from Libraries in the top-right corner of the Frames tab.

![Hide calls in Kotlin classes](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin_debug_coroutines_frames_f.png)



When examining the internal operations of a coroutine, you can also use other analysis aids like watches and arbitrary expression evaluation.

### Get coroutines dump

If you need a report containing the state of each coroutine and its stack, use a [thread dump](thread-dumps.html). IntelliJ IDEA's thread dump includes Java platform threads, virtual threads, and Kotlin coroutines.

  * On the Debug tool window's toolbar, click ![More](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg) More, then select ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.dump.svg) Get Thread Dump.


![The More button on the Debug tool window toolbar](https://resources.jetbrains.com/help/img/idea/2025.3/ij_debug_more.png)

24 July 2025

[Run Kotlin interactively](run-kotlin-interactively.html)[Ktor](ktor.html)
