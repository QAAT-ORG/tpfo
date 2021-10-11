# Track process from outside

Track as much as you can for single proceess without directly
interacting with it. But the process will be started by this process. Think of this as some kind of process wrapper.

Goals:
* Cover as many stats as possible
* Cross platform ( but linux first )
* Should have a minimal impact on performance of observed process

Readings or refs:
* https://pingcap.com/blog/how-to-trace-linux-system-calls-in-production-with-minimal-impact-on-performance
* https://perf.wiki.kernel.org/index.php/Main_Page
* https://www.youtube.com/watch?v=D53T1Ejig1Q
* https://ebpf.io/
* https://www.brendangregg.com/

Will be written in Rust.