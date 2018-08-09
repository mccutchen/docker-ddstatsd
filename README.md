# docker-ddstatsd

A containerized version of [mreiferson/ddstatsd][]:

> `ddstatsd` is a UDP proxy that takes a JSON configuration file with regex-
based rules to rewrite incoming metric names and add tags, outputing to the
local `dd-agent` in its custom statsd format.

In short, `ddstatsd` translates "plain" statsd metrics into tagged metrics for
use with DataDog, according to a set of rules. See [rules.cfg][] in
[mreiferson/ddstatsd][] for an example.

## Example usage

A valid rule configuration file must be placed into the container at
`/ddstatsd/rules.cfg`. A valid `-destination-address` pointing to the DataDog
statsd agent must be given as part of the `docker run` command:

```bash
docker run -d -v $PWD/rules.cfg:/ddstatsd/rules.cfg mccutchen/ddstatsd:latest -destination-address=$HOST:8125
```

[mreiferson/ddstatsd]: https://github.com/mreiferson/ddstatsd
[rules.cfg]: https://github.com/mreiferson/ddstatsd/blob/master/rules.cfg
