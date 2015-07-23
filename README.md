# puppet-hieradata

Puppet hieradata for Minestack

This is just an example configuration. This repo should be forked and modified to match your network configuration

## How to use

Install Puppet

```sh
rpm -ivh https://yum.puppetlabs.com/puppetlabs-release-el-7.noarch.rpm
yum install puppet
gem install librarian-puppet
```

Remove default puppet configurations

```sh
rm -rf /etc/puppet
```

Git Clone

```sh
git clone https://github.com/Minestack/puppet-hieradata.git /etc/puppet/
```

Run librarian Puppet

```sh
cd /etc/puppet
librarian-puppet install
librarian-puppet update
```

Run Puppet

```sh
puppet apply /etc/puppet/manifests/site.pp
```

Puppet will now run automatically every 30 minutes to ensure everything is configured correctly.
