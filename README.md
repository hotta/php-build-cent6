# How to build php56 on CentOS 6.9

```bash
$ sudo yum install -y install git epel-release
$ sudo yum -y install ansible
$ git clone https://github.com/hotta/php-build-cent6.git
$ cd php-build-cent6
$ ansible-playbook -i hosts site.yml --tags=base,php56
$ cd
$ rpmbuild --rebuild ~/rpmbuild/SRPMS/php56-php-5.6.35-1.remi.src.rpm
```

# How to build php70 on CentOS 6.9

```bash
$ sudo yum install -y install git epel-release
$ sudo yum -y install ansible
$ git clone https://github.com/hotta/php-build-cent6.git
$ cd php-build-cent6
$ ansible-playbook -i hosts site.yml --tags=base,php70
$ cd
$ rpmbuild --rebuild ~/rpmbuild/SRPMS/php70-php-7.0.29-1.remi.src.rpm
```
