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

## Output

Future versions of this will have a properly formatted output

```
$ BOSH_ENVIRONMENT=lite ./medic scalablesyslog
adapter/8497540d-74cd-4fdc-98cc-e0886b5004ac: {"drainCount":1}
adapter/8143e1cb-39e1-49c8-823c-c0d873aa9831: {"drainCount":1}
adapter/8f699d67-687b-4a56-9bdd-1d3e23a2c080: {"drainCount":1}
scheduler/872543ba-ca69-4926-95d8-6f90c4672038: {"adapterCount":3,"blacklistedOrInvalidUrlCount":0,"drainCount":1}
```

[loggregator-release]:     https://github.com/cloudfoundry/loggregator
[scalable-syslog-release]: https://code.cloudfoundry.org/scalable-syslog-release
