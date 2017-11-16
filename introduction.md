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

#### Kerckhoffs' principle [\[1\]](#References)

    A crypto system should be secure even if the attacker (Eve) Knows all the
    details about the system, with the exception of the secret
    key.

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

### Attacks on Substitution cipher

Q: Is this substitution cipher secure? How can we attack the cipher?

#### Brute-force attack or exhaustive key search

The key space for Substitution Cipher is `N!` (factorial of n), N in this case
means the number of letters. 26!, that is something between 2^88 ans 2^89. On
the classes I'm taking it says is not possible with the current computation
power break a 2^88 key, because the key space is too large. Maybe this
information is outdated. I'll update this part when I have confirmation on
this.

#### Letter frequence analysis

If an atacker intercepts a ciphertext encrypted with substitution cypher, we
take a look on the frequence of the letters in the language we think the
message is written in. This will give us good hint about the plaintext.

### Classification of attacks

As we could see here, there are often many possible attack approaches (attack
vector)

```
cryptoanalysis
|\
v +->Analitical attacks
Brute-force
Social engineering
Implementation attacks
Side-channel attacks
```

As an attacker you can try all possible approaches to attack a crypto system.
But as a defender you must to defend your system against all of them.

## References

[1] - https://en.wikipedia.org/wiki/Kerckhoffs's_principle How can we attack the cipher?
[2] - https://www.keylength.com/en/compare/
[3] - https://en.wikipedia.org/wiki/Substitution_cipher#Security_for_simple_substitution_ciphers
