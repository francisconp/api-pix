### How to check if a private key belongs to a public certificate



$ openssl x509 -noout -modulus -in pub.pem |  openssl md5
$ openssl rsa -noout -modulus -in key.pem | openssl md5
