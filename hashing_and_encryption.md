# password hashes

An encryption function takes a string as input (we call it plaintext) and produces an encrypted string as output (we call it ciphertext).

A hash function takes a string as input (like a password or message) and produces a fixed-length hash value as output (we call it a message digest).

For example, the RSA algorithm is an encryption algorithm, and it has a variable-length output.

The MD5 algorithm is a hash algorithm, and it has a fixed-length output.

When I log into my computer, I think that my computer calculates a password hash for the password that I enter, and compares it with the password hash that's stored on file. Since the password hash is fixed-length, it doesn't tell you anything about the length of the actual password.

The MD5 algorithm is really interesting.

I have an open-source implementation of the RSA algorithm on my Github, in the repository called "rsa".
