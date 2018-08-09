# docker-ddstatsd

A containerized version of [mreiferson/ddstatsd][]:

> `ddstatsd` is a UDP proxy that takes a JSON configuration file with regex-
based rules to rewrite incoming metric names and add tags, outputing to the
local `dd-agent` in its custom statsd format.

In short, `ddstatsd` translates "plain" statsd metrics into tagged metrics for
use with DataDog, according to a set of rules.

See [rules.cfg][] in [mreiferson/ddstatsd][] for an example.

[mreiferson/ddstatsd]: https://github.com/mreiferson/ddstatsd
[rules.cfg]: https://github.com/mreiferson/ddstatsd/blob/master/rules.cfg
