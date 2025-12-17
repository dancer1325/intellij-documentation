[//]: # (Source: https://www.jetbrains.com/help/idea/read-the-profiling-report.html)
[//]: # (Downloaded: 2025-12-17 19:56:48)

## Navigate the snapshot

By default, library and framework methods are shown collapsed. You can expand the collapsed calls by clicking the expand button in the corresponding frame.

![Pointing at the 'expand' button in a flame graph's frame](https://resources.jetbrains.com/help/img/idea/2025.3/collapsed-flame-graph-calls.png)

When you focus on a specific method in a tab of the Profiler tool window, IntelliJ IDEA opens the corresponding source in the editor. Also, you can right-click it and select another Profiler tool window tab to open it in.

![Jumping between tabs in the Profiler tool window](https://resources.jetbrains.com/help/img/idea/2025.3/focus-on-method-call.png)

### Threads

The profiling data in the Profiler tool window tabs is grouped by thread. You can select to view merged data for the entire process (All threads merged) or select a specific thread for closer investigation.

### Show threads

By default, the list of threads is hidden, and the data is shown for all threads combined.

  * To select a particular thread or review the list of threads, click the Show Threads View in the left-hand toolbar. 




In-editor profiler hints always show the combined runtime for all threads.

![The Threads panel in the Profiler tool window](https://resources.jetbrains.com/help/img/idea/2025.3/profiler-threads.png)

The threads are listed on the left-hand side of the Profiler tool window and sorted by the number of collected samples. Thus, you can find the most busy threads at the top of the list.
