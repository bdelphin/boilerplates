# Hide Apache version

Let's make Apache looks like Microsoft IIS (or whatever).

```
sudo apt update
sudo apt install -y libapache2-mod-security2
sudo a2enmod security2
```

Edit apache config `/etc/apache2/conf-available/security.conf` :

```
# edit :
ServerTokens Full
ServerSignature Off

# add :
SecServerSignature Microsoft-IIS/10.0
```

You can hide everything with :

```
SecServerSignature " "
```
