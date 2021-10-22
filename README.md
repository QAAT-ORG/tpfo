# Track process from outside

Track as much as you can for single proceess without directly
interacting with it. But the process will be started by this process. Think of this as some kind of process wrapper.

Track = Trace ?

Goals:
* Cover as many stats as possible
* Cross platform ( but linux first ) - questioning this now :)
* Configurable ( what to track, who to track)
* Should have a minimal impact on performance of observed process

Readings or refs:
* https://pingcap.com/blog/how-to-trace-linux-system-calls-in-production-with-minimal-impact-on-performance
* https://perf.wiki.kernel.org/index.php/Main_Page
* https://www.youtube.com/watch?v=D53T1Ejig1Q
* https://ebpf.io/
* https://www.brendangregg.com/
  * https://www.brendangregg.com/perf.html
  * https://www.brendangregg.com/blog/2018-10-08/dtrace-for-linux-2018.html
* https://stackoverflow.com/questions/46674444/is-it-possible-to-run-linux-perf-tool-inside-docker-container
  * https://stackoverflow.com/questions/38927895/how-do-you-get-debugging-symbols-working-in-linux-perf-tool-inside-docker-contai
  * https://stackoverflow.com/questions/44745987/use-perf-inside-a-docker-container-without-privileged

Seems perf_events is so cool for linux, we'll see when we start playing around this.

Interesting project too is pixie ( might serve as inspiration ) : https://github.com/pixie-io/pixie

It uses BPF .. ( which also supports kprobes, uprobes, traces )

Little worries about data output of perf if process is long running, not so much for performance, but I feel storage can be a problem,
don't know anything now, but we'll get info when this gets a bit bigger than a README.

2 stats that matter :
* Flame graphs (Generally hot spots)
* Time series tace info of observed process per thread ( if possible, would be great, think it's possible )

---

Will be written in Rust or C++ .
