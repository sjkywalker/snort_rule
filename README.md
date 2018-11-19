# Snort Rule

Modifies the suricata rules file to `alert` when accessing certain websites.

## Getting started

### Overview

* Detects following websites
    * gilgil.net
    * www.gilgil.net
    * test.gilgil.net
    * snoopspy.com
    * naver.com
    * twitter.com
    * facebook.com
* `HTTP` packets identified by http request header `"Host: "` field
* `HTTPS` packets (`TLS` encrypted) identified by dns query

### Program flow

Uses the `suricata` program.

### Development Environment

```txt
$ uname -a
Linux ubuntu 4.15.0-36-generic #39~16.04.1-Ubuntu SMP Tue Sep 25 08:59:23 UTC 2018 x86_64 x86_64 x86_64 GNU/Linux
```

### Prerequisites

The following commands will install some of the essential packages.

```bash
$ apt install suricata
```

Also, modify the `suricata.yaml` file and `test.rules` prior to running `suricata`.

## Running the program

### Configuration

### Run

Get used to the `suricata` program.

Format

```bash
$ suricata -c <path_to_yaml_file>  -i <interface>
```

Example

```bash
$ suricata -c /etc/suricata/suricata.yaml -i eth0
```

### Get alerts

Get the alerts by reading the `fast.log` file.

Format

```bash
$ tail -f <path_to_fast.log>
```

Example

```bash
$ tail -f /var/log/suricata/fast.log
```

You might need root priviledges to read and write, execute files related to `suricata`.

## Acknowledgements

* [Suricata](https://suricata-ids.org/)
* [Suricata Alerts](https://suricata.readthedocs.io/en/suricata-4.0.5/make-sense-alerts.html)

## Authors

* **James Sung** - *Initial work* - [sjkywalker](https://github.com/sjkywalker)
* Copyright © 2018 James Sung. All rights reserved.
