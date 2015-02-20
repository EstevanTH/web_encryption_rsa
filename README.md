# Web Encryption w/ RSA
This project is a Web-based RSA encryption system for PHP and JavaScript.

*The project has not begun yet.*

*Your help is welcome.*

## Introduction
A Web-based RSA encryption system allows to efficiently obfuscate sensitive information when the usage of HTTPS is impossible. Not having a valid SSL certificate is not a big problem anymore when exchanging passwords, email adresses, etc. For instance this is especially true for clients using an unencrypted WiFi access.

Unlike other cheap encryptions using a single key, RSA encryption uses a set of keys (a *private* key and a *public* key). As long as the *private* key remains secret, the encryption is strong:

1. The server sends the *public* key to the client.
2. The server sends information, encrypted with the *private* key. The client decrypts it using the *public* key.
3. The client sends information, encrypted with the *public* key. The server decrypts it using the *private* key.

**Warning:** SSL certificates are a guarantee that the server is the expected server. Invalid certificates display a warning on clients' Web browser. **Man-in-the-middle attacks** cannot be avoided without an SSL certificate.

## Project contents
The project is composed of 3 parts:
* a *PHP* library with documentation and examples
* a *JavaScript* library with documentation and examples (especially about usage in forms)
* a *C++* program that generates pairs of RSA keys

## About the project
The project is based on [RSA source code from OpenSSL](https://github.com/openssl/openssl/tree/master/crypto/rsa).
