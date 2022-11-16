### How to check if a private key belongs to a public certificate


``` shell
PRIVATE_MD5=$(openssl x509 -noout -modulus -in pub.pem |  openssl md5)
PUBLIC_MD5=$(openssl rsa -noout -modulus -in key.pem | openssl md5)
echo -e "$PRIVATE_MD5\n$PUBLIC_MD5"
```

The result of both variables needs to be equal.
