# puppet-hieradata
Puppet hieradata for Minestack

## Example hiera.yaml

```yaml
---
:backends:
  - yaml
:yaml:
  :datadir: /etc/puppet/environments/production/hieradata
:hierarchy:
  - "%{::clientcert}"
  - common
```
