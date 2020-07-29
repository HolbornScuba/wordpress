# WordPress
Holborn Wordpress deployment

This repo should manage the deployment of WordPress to the holborn site

Encrypting the secrets
```
echo -n 'passphrase' | gpg --symmetric --batch --yes --passphrase-fd 0 --cipher-algo AES256 -o env.yaml.gpg env.yaml
```
Decrypting the secrets
```
echo -n 'passphrase' | gpg --decrypt --batch --yes --passphrase-fd 0 --cipher-algo AES256 -o env.yaml env.yaml.gpg
```
