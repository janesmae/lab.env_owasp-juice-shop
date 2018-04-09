# OWASP Juice Shop lab setup

Lab setup for <number_of_people>. Configurable from setup_lab.yml using docker
to host. Make sure, <target_host> is in ansible inventory and has python installed.

```sh
ssh root@<target_host> 'apt-get install python -y'
ansible-playbook setup_lab.yml
```

For letsencrypt wildcard ssl certificate use the following command:

```sh
certbot certonly -d <domain> -d *.<domain>  --server https://acme-v02.api.letsencrypt.org/directory --manual --preferred-challenges dns-0
```

## Links

- [OWASP Juice Shop Project](https://www.owasp.org/index.php/OWASP_Juice_Shop_Project)
- [Owasp Juice Shop Sourcecode](https://github.com/bkimminich/juice-shop)
