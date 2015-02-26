---
id: whats-new
---

Most of the changes of LTTng 2.6 are bug fixes, making the toolchain
more stable than ever before. Still, LTTng 2.6 adds some interesting
features.

LTTng 2.5 already supported the instrumentation and tracing of
[Java applications](#doc-java-application) through `java.util.logging`
(JUL). LTTng 2.6 goes one step further by supporting
<a href="https://logging.apache.org/log4j/1.2/" class="ext">Apache log4j 1.2</a>.
The new log4j domain is selected using the `--log4j` option in various
commands of the `lttng` tool.

LTTng-modules has supported system call tracing for a long time,
but until now, it was only possible to record either all of them,
or none of them. LTTng 2.6 allows the user to record only a specific
subset of system call events, e.g.:

<pre class="term">
lttng enable-event --kernel --syscall open,fork,chdir,pipe
</pre>

Finally, the `lttng` command line tool cannot only communicate with
humans as it used to do, but also with machines thanks to its new
[machine interface](#doc-mi) feature.