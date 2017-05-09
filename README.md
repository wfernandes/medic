# medic

This is a tool to aggregate the data retrieved from the health endpoints from
various CF components.

Currently, there are a few components in the
[loggregator][loggregator-release] and the
[scalable-syslog-release][scalable-syslog-release] that have health endpoints.

As the number of components increase, it would be nice to have a tool that can
aggregate the health of the endpoints to provide faster troubleshooting rather
than ssh'ing into each vm.

## Usage

```
./medic <deployment_name>

For example,
./medic scalablesyslog
```

[loggregator-release]:     https://github.com/cloudfoundry/loggregator
[scalable-syslog-release]: https://code.cloudfoundry.org/scalable-syslog-release
