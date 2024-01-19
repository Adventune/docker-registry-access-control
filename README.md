# docker-registry-access-control

This repository contains the code files for my blog post at https://samukupiainen.fi/blog/docker-registry-access-control/.

## openssl commands:

```bash
# Generate private key
openssl genpkey -algorithm RSA -out ./auth-config/auth.key

# Create a certificate signing request
openssl req -new -key ./auth-config/auth.key -out csr.pem # Answer the questions for the self signed certificate

# Generate the certificate
openssl x509 -req -in csr.pem -signkey ./auth-config/auth.key -out ./auth-config/auth.pem
```
