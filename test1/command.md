Hosts file:

```
---
HOSTS:
  centos7-64-1:
    pe_dir:
    pe_ver:
    pe_upgrade_dir:
    pe_upgrade_ver:
    hypervisor: vmpooler
    platform: el-7-x86_64
    template: centos-7-x86_64
    roles:
    - master
    - agent
    - dashboard
    - database
CONFIG:
  nfs_server: none
  consoleport: 443
  pooling_api: http://vmpooler.delivery.puppetlabs.net/
```

Command:

in `puppet/acceptance`

`BEAKER_HOSTS=centos7-pe.yml SHA=d33a1fddd412fce059fdc68127a0b9b31c0bfe98 TEST=tests/security/cve-2013-1652_improper_query_params.rb bundle exec rake ci:test:aio`
