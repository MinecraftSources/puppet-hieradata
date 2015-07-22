# puppet-hieradata
Puppet hieradata for Minestack

## How to use

Install Puppet

```sh
rpm -ivh https://yum.puppetlabs.com/puppetlabs-release-el-7.noarch.rpm
yum install puppet
```

Create hiera.yaml in /etc/puppet

```yaml
---
:backends:
  - yaml
:yaml:
  :datadir:" /etc/puppet/environments/%{::environment}/hieradata"
:hierarchy:
  - "%{::clientcert}"
  - common
```

Create environments

```sh
mkdir /etc/puppet/environments
```

Git Clone

```sh
git clone https://github.com/Minestack/puppet-hieradata.git /etc/puppet/environments/production
```

Run librarian Puppet

```sh
cd /etc/puppet/environments/production
librarian-puppet install
librarian-puppet update
```

Run Puppet

```sh
puppet agent -t
```
