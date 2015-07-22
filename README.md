# puppet-hieradata
Puppet hieradata for Minestack

## How to use

Install Puppet

```sh
rpm -ivh https://yum.puppetlabs.com/puppetlabs-release-el-7.noarch.rpm
yum install puppet
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
puppet agent -t
```
