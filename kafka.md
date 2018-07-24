# kafka

## Log Message

Here is one log message:

```
[2018-07-23 18:14:23,854] INFO Recovering unflushed segment 0 in log __consumer_offsets-8. (kafka.log.Log)
```

```
[TIME] LEVEL MESSAGE (CLASS)
```

## Regex

```
^(?<time>\[[0-9]+-[0-9]+-[0-9]+ [0-9]+:[0-9]+:[0-9]+,[0-9]+\])\s*(?<level>\S+)\s*(?<message>[\s\S]*?)\s*(?=\g<time>|\Z)
```

http://rubular.com/r/PX1KVfvHHT

```
time	[2018-07-23 18:14:23,854]
level	INFO
message	Recovering unflushed segment 0 in log __consumer_offsets-8. (kafka.log.Log)
```
