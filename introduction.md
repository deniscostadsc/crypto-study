# Introduction

Today a lot of service we use depends on cryptography.

Few exampĺe of modern application of cryptography:

* - Bank Cards
* - Cards
* - Enigmail (Thunderbird)
* - GnuGPG
* - SSL
* - Secure Shell (SSH)
* - TruCrypt
* - VPN
* - Whatsapp
* - [HDCP](https://en.wikipedia.org/wiki/High-bandwidth_Digital_Content_Protection)
* - e-Passaport

## Classification

Cryptology splits in two different branches Cryptography and Cryptanalysis.
First are focused in the design of crypto system and the second focused on
analysis and possible breaches o crypto systems. Cryptography has many
branches, the most known are symmetric and asymmtric algorithms and crypto
protocols. There are more branches below cryptography, but this course is going
to focus on those three.

```
+-*-*-*-*-*+
| Security |
+-*-*-*+*-*+
       |
+------v-----+
| Cryptology |
+------+-----+------------+
       |                  |
+------v-------+      +---v-----------+
| Cryptography |      | Cryptanalysis |
+------+----+--+-+    +---------------+
       |    |    |
       |    |    +-------------------+
       |    +--------------+         |
+------v---------------+   |  +------v-----------+
| Symmetric Algorithms |   |  | Crypto Protocols |
+----------------------+   |  +------------------+
                    +------v---------------+
                    | Asymmetric Algorithms |
                    +----------------------+
```

Security fields is much bigger then cryptography, but most of security systems
are strongly based on cryptography.

## Symmetric setup

```
+-------+                                      +-----+
| Alice |             +-*-*-*-*-*+             | Bob |
+-----+-+ X  +---+  Y | Insecure | Y  +---+  X +-^---+
      +------| e |----> Channel  +----| d |------+
             +-^-+    +-*-*-+-*-*+    +-^-+
               |            |           |
             +-+-+          |         +-+-+
             | k |          | Y       | k |
             +-+-+       +--v--+      +-^-+
               |         | Eve |        |
               |         +-----+        |
               |                        |
               |       +-*-*-*-*-+      |
               +-------> Secure  +------+
                       | Channel |
                       +-*-*-*-+-+
                  // Key Transference //

Alice - Sender
Bob - Receiver
Eve - Attacker
X - Plaintext
Y - Ciphertext
e - Encryptio Function
d - Decryption Function
k - Secret Key
```

The fluxogram above, shows Alice, sending a message "X" (Plaintext) to Bob over
an insecure channel. On the botton we can see Eve tht got the message "Y"
(Ciphertext), which is the cyphertext for "X". On the "e" and "d" blocks we
have encryption and decryption functions, respectively. And both encryption and
decription functions dependes on a shared key between both Alice and Bob. The
"Secure Channel" block is one way to share the key between Alice and Bob.

`|K|` is one way of represent the key space, that is the number of possible
keys.

### Public crypto algorithms x Secret crypto algorithms

It could be intuitive to think that is a good idea to keep these functions
secret, and that was a common sense years ago.

    In practice: Never use an crypto algorithms that wasn't heavily tested or
    are not public.

#### Kerckhoffs' principle

    A crypto system should be secure even if the attacker (Eve) Knows all the
    details about the system, with the exception of the secret
    key[\[1\]](#References).

## Substitution cipher

Substitution Cipher is a anciente cipher, that mainly operates on letter, not
on bits and bytes. The ideia behind it it to replace every plaintext letter by
a fixed ciphertext letter.

Example:

```
A -> l
B -> d
C -> w
.
.
.
```

e.g. e(ABBA) -> lddl

Q: Is this cipher secure? How can we attack the cipher?

## Attacks

### Brute-force

## References

[1] - https://en.wikipedia.org/wiki/Kerckhoffs's_principle How can we attack the cipher?
