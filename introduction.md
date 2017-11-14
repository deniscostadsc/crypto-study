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
+-------+                                         +-----+
| Alice |             +-*-*-*-*-*-*-+             | Bob |
+-------+ X  +---+  Y |   Insecure  | Y  +---+  X +-^---+
        +----| e |---->   Channel   +----| d |------+
             +---+    +-*-*-*-+-*-*-+    +---+
                              |
                              |
                              | Y
                           +--v--+
                           | Eve |
                           +-----+
```

On the "e" and "d" block we have encryption and decryption functions,
respectively. It could be intuitive to think that is a good idea to keep these
function secret, and that was a common sense years ago.

    In practice: Never use an untested (non-public) crypto algorithm!

## Substitution cipher

## Attacks
