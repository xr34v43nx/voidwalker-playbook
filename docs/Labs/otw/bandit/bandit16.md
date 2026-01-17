# Goal
The password for the next level can be retrieved by submitting the password of the current level to **port 30001** on localhost using SSL/TLS encryption.

## What to learn
From the levels description page it lists Secure Socket Layer/Transport Layer Security and the OpenSSL Cookbook - Testing with OpenSSL as helpful reading.  The previous level required the password be sent through cleartext over nc, This level requires an SSL handshake in order for the information to be passed. A definite close examination of --help and man  <tool> will be a requirement to reach the next level.

[!critical] greater detail of SSL/TLS needs to explored at a later date. (added to todo list)