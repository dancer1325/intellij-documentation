[//]: # (Source: https://www.jetbrains.com/help/idea/custom-profiler-configurations.html)
[//]: # (Downloaded: 2025-12-17 19:23:41)

## Async Profiler

Async profiler is compatible with HotSpot JVM and [some other Java runtimes](https://github.com/jvm-profiling-tools/async-profiler/blob/master/README.md#async-profiler).

On Windows and macOS, the profiler works out of the box. If you are on Linux, you have to adjust kernel options before you start profiling.

### Adjust kernel options on Linux

  1. Adjust perf_event_paranoid. This option controls the use of the performance events data by non-root users.

Set the value to be less than 2 to let the profiler collect performance information without root privileges:

sudo sh -c 'echo 1 >/proc/sys/kernel/perf_event_paranoid' 

  2. Adjust kptr_restrict. This option sets restrictions on exposing kernel addresses.

To have kernel symbols properly resolved, disable the protection offered by _kptr_restrict_ by setting its value to 0:

sudo sh -c 'echo 0 >/proc/sys/kernel/kptr_restrict' 




By default, these changes affect your current OS session only. To keep the settings across system reboots, run:

sudo sh -c 'echo kernel.perf_event_paranoid=1 >> /etc/sysctl.d/99-perf.conf' sudo sh -c 'echo kernel.kptr_restrict=0 >> /etc/sysctl.d/99-perf.conf' sudo sh -c 'sysctl --system' 

### Configuration options

You can find the detailed explanations of Async Profiler configuration in the [official documentation on GitHub](https://github.com/jvm-profiling-tools/async-profiler).

Option| Description  
---|---  
Agent Options| The options that will be passed to the agent. They can be used, for example, to enable wall-clock profiling, or adjust the sampling interval.  
Agent| The agent that will be used for profiling.
