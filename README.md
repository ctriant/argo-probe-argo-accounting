# argo-probe-argo-servicestatus

A generic probe to check service status. The probe calls /status endpoint and infers from the response if the service is up and running.

## Synopsis

The probe has two required arguments: `timeout` and `url`.

```
# /usr/libexec/argo/probes/argo-servicestatus/check_status.py --help
usage: check_status.py -t TIMEOUT -u URL [-h]

ARGO probe that checks service status.

required arguments:
  -t TIMEOUT, --timeout TIMEOUT
                        timeout
  -u URL, --url URL     service url

optional arguments:
  -h, --help            show this help message and exit
```

Sample execution of `check_status.py`

```
# /usr/libexec/argo/probes/argo-servicestatus/check_status.py -u https://wiki.eoscfuture.eu -t 30
OK - Service available

```
