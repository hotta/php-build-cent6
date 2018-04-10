# How to build php56 / php70 on CentOS 6.9

## Common procedure

```bash
$ sudo yum install -y install git epel-release
$ sudo yum -y install ansible
$ git clone https://github.com/hotta/php-build-cent6.git
$ cd php-build-cent6
```

## To build php56

```bash
$ ansible-playbook -i hosts site.yml --tags=base,php56-all
$ cd
$ rpmbuild --rebuild ~/rpmbuild/SRPMS/php56-php-5.6.35-1.remi.src.rpm
```

## To build php70

# for PHP70

```bash
$ ansible-playbook -i hosts site.yml --tags=base,php70-all
$ cd
$ rpmbuild --rebuild ~/rpmbuild/SRPMS/php70-php-7.0.29-1.remi.src.rpm
```
