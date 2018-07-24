# Java

## Example 1

The default log message pattern for SpringBoot apps looks like following:

### Log Message

```
2018-07-24 07:37:02.702  INFO 1 --- [           main] o.s.b.w.e.u.UndertowServletWebServer     : Undertow started on port(s) 8080 (http) with context path ''
```

```
TIME LEVEL PID --- [THREAD] CLASS : MESSAGE
```

### Regex

```
^(?<time>\d+(?:-\d+){2}\s+\d+(?::\d+){2}\.\d+)\s*(?<level>\S+) (?<pid>\d+) --- \[(?<thread>[\s\S]*?)\] (?<class>\S+)\s*:\s*(?<message>[\s\S]*?)(?=\g<time>|\Z)
```

You can see it in action here: http://rubular.com/r/T8xUSnXeXz

The Regex will parse the above message like this:

```
time	2018-07-24 07:37:02.702
level	INFO
pid	1
thread	main
class	o.s.b.w.e.u.UndertowServletWebServer
message	Undertow started on port(s) 8080 (http) with context path ''
```
