[//]: # (Source: https://www.jetbrains.com/help/idea/using-profiler-labels.html)
[//]: # (Downloaded: 2025-12-17 20:05:42)

## Adding labels

The `runtime/pprof` package has several new functions that you can use to add labels. The most popular is the `Do` function. The `Do` function takes context, adds labels to this context, and passes new context to the f function.

func Do(ctx context.Context, labels LabelSet, f func(context.Context))

The `Do` function writes labels only for the current goroutine. If you create new goroutines in the f function, you can pass the context as an argument.

func main() { ctx := context.Background() for i := 0; i < 10; i++ { labels := pprof.Labels("path", "/api/profile", "userId", strconv.Itoa(rand.Intn(100))) go pprof.Do(ctx, labels, f) } time.Sleep(time.Second) }
