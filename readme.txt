DSU INFA 723 HOMEWORK 3
SUBMITTED BY JOSHUA BARTHOLOMEW


QUESTION 1
==========

For parts a-c, I used the command "$ openssl x509 -in cert.cer -text -noout" [1]. The output from the command is included below.

Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number:
            b9:7d:c1:51:ed:a0:4f:ce
        Signature Algorithm: sha256WithRSAEncryption
        Issuer: C = US, ST = SD, L = Madison, O = DSU, OU = INFA723, CN = Homework, emailAddress = yong.wang@dsu.edu
        Validity
            Not Before: Mar 22 02:18:53 2017 GMT
            Not After : Mar 22 02:18:53 2018 GMT
        Subject: C = US, ST = SD, L = Madison, O = DSU, OU = INFA723, CN = Homework, emailAddress = yong.wang@dsu.edu
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                RSA Public-Key: (2048 bit)
                Modulus:
                    00:d1:80:5e:8c:de:f2:9f:14:5a:93:60:82:fb:2f:
                    5f:2e:51:12:12:76:89:6b:ec:62:93:db:e0:09:b5:
                    af:07:0e:77:51:5d:08:ab:99:44:27:dd:5d:0a:b4:
                    6d:f1:27:98:74:5d:12:b2:59:44:5d:0a:2c:46:bb:
                    76:78:a9:c0:01:5f:1f:ca:91:cd:1c:2f:02:95:f1:
                    0f:cb:2e:8f:c9:bc:c4:db:b5:b8:c8:cc:71:12:72:
                    f5:67:39:db:8d:04:d8:50:77:14:a4:c8:66:c2:d5:
                    9f:d6:6c:52:c1:05:da:6d:3d:b0:86:8a:69:89:05:
                    22:c7:96:31:d6:4f:16:38:47:b7:7b:65:d1:63:07:
                    57:42:1a:98:f3:6e:b8:bb:9c:d9:0f:bc:9c:5c:d4:
                    c2:e4:ca:a4:b5:ed:32:ea:f1:0d:4c:07:07:ec:fc:
                    3d:3e:20:60:1d:32:3a:f4:cb:04:0b:28:cc:24:7c:
                    46:23:6b:73:e6:a2:1e:7e:db:18:e2:84:95:f1:33:
                    26:2f:b9:1b:4a:98:6d:44:a5:d9:f6:95:f9:94:74:
                    ad:3a:77:43:2c:52:6e:3e:c3:e8:bb:68:ce:bf:e4:
                    3d:a7:db:4e:08:70:2b:43:69:59:e2:a8:db:13:ff:
                    81:06:74:95:c5:74:f4:9b:f1:ba:4b:2e:7e:b8:a1:
                    d4:5f
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Subject Key Identifier:
                68:B9:B9:79:1C:28:60:17:45:50:C6:C8:FC:59:64:ED:1A:A1:1F:A6
            X509v3 Authority Key Identifier:
                keyid:68:B9:B9:79:1C:28:60:17:45:50:C6:C8:FC:59:64:ED:1A:A1:1F:A6

            X509v3 Basic Constraints:
                CA:TRUE
    Signature Algorithm: sha256WithRSAEncryption
         99:a7:02:86:fc:9f:25:2c:14:d9:b6:55:c4:33:ce:46:e7:10:
         a8:1b:37:ea:4b:f0:8d:46:9c:4d:34:ef:0a:3f:0e:1b:a0:2b:
         69:52:f5:d4:64:0f:3b:51:e2:fc:3c:89:1d:fc:14:17:fd:5a:
         84:b0:44:cd:80:a7:08:7c:69:92:3f:f1:70:b6:91:74:86:47:
         37:da:e2:78:a5:65:6f:76:c3:0e:49:10:94:cf:26:dc:31:d6:
         18:f5:92:85:4d:41:ed:e0:f7:30:2d:8a:a3:f0:fa:81:2d:60:
         5f:60:08:7e:21:fa:ee:88:25:b5:13:3a:ac:fa:ed:30:3b:1d:
         74:56:f1:91:90:e7:1d:ec:46:fd:71:12:b6:68:a7:bd:1c:76:
         5b:dc:43:73:c5:08:7a:a3:f1:10:b3:2a:af:f0:6f:ee:b7:f5:
         da:49:7a:79:db:c2:b3:b2:dd:f8:0e:60:ff:3a:7b:4a:9c:69:
         8a:dd:d0:6d:ca:ec:da:ba:5a:1f:59:48:b1:29:66:d3:46:26:
         27:f6:fc:0a:a3:33:5c:03:0b:24:77:36:dc:e8:2b:84:be:c7:
         b0:63:ba:22:05:bb:db:43:6c:c2:2a:11:2b:83:66:3a:ad:69:
         5d:e3:e1:31:e5:5e:d5:d4:c6:b6:26:6e:7c:c6:1c:f1:46:0c:
         6d:44:ad:8f

a) Signature Algorithm: sha256WithRSAEncryption

b) Public Key Algorithm: rsaEncryption

c) RSA Public-Key: (2048 bit)


For part d, I used the smime(1) manual page to craft the proper decryption command [2]. The command used was "$ openssl smime -decrypt -binary -aes-256-cbc -in tr
ackbcipher.txt -inform DER -inkey prikey.pem -out trackbdecrypted.txt".

d) Decrypted message:

"Ron Rivest grew up in Niskayuna, New York, a suburb of Schenectady. He attended public schools and graduated from the Niskayuna High School in 1965. He graduated from Yale University in 1969 with a B.A. in mathematics, and from Stanford University in 1973 with a PhD in Computer Science. He learned from the best: his PhD supervisor was Turing Award recipient Robert Floyd, and he worked closely with Turing Award laureate Don Knuth.
Following graduate study he accepted a post-doctoral position at INRIA in Rocquencourt, France before taking a job at MIT, where he has been ever since. He currently holds the Andrew and Erna Viterbi professorship in the Department of Electrical Engineering and Computer Science.
At MIT he met Leonard M. Adleman and Adi Shamir, who collaborated with Ron on their fundamental advance in cryptography. They were inspired by a 1976 paper [4] by cryptographers Whitfield Diffie and Martin Hellman discussing several new developments in cryptography. It described ways for the sender and receiver of private messages to avoid needing a shared secret key, but it did not provide any realistic way to implement these concepts. Rivest, Shamir, and Adleman presented practical implementations in their 1977 paper, �A method for obtaining digital signatures and public-key cryptosystems,� [1] which showed how a message could easily be encoded, sent to a recipient, and decoded with little chance of it being decoded by a third party who sees it.
The method, known as Public Key Cryptography, uses two different but mathematically linked keys: one public key used to encrypt the message, and a completely different private key used to decrypt it. The encrypting key is made public by individuals who wish to receive messages, but the secret decrypting key is known only them. The two keys are linked by some well-defined mathematical relationship, but determining the decryption key from its publically available counterpart is either impossible or so prohibitively expensive that it cannot be done in practice. The �RSA� method (from the first letters of the names of the three authors) relies on the fact that nobody has yet developed an efficient algorithm for factoring very large integers. There is no guarantee, however, that it will be difficult forever; should a large quantum computer ever be built, it might be able to break the system.
A detailed discussion of the theory and practice behind RSA can be found here. The computer code to implement it is quite simple, and as long as suitably large integer keys are used, no one knows how to break an encoded message.
RSA is used in almost all internet-based commercial transactions. Without it, commercial online activities would not be as widespread as they are today. It allows users to communicate sensitive information like credit card numbers over an unsecure internet without having to agree on a shared secret key ahead of time. Most people ordering items over the internet don�t know that the system is in use unless they notice the small padlock symbol in the corner of the screen. RSA is a prime example of an abstract elegant theory that has had great practical application.
After developing the basic method in 1977, the three Turing Award recipients founded RSA Data Security in 1983. The company was later acquired by Security Dynamics, which was in turn purchased by EMC in 2006. It has done cryptographic research, sponsored conferences, shown how earlier encryption systems could be compromised, and spun off other companies such as Verisign. Rivest thus demonstrated that he could move easily between theory and practice. When the 1983 patent on RSA [2] was about to expire, RSA Data Security published all the details of its implementation so that there would be no question that anyone could create products incorporating the method.
The three Turing Award recipients were not aware that a similar method had been developed years before by British mathematician Clifford Cocks, who extended the even earlier work of James H. Ellis. Cocks was doing his encryption work at the Government Communications Headquarters (GCHQ), so it was classified as secret and not released until 1997, twenty years after Rivest, Adleman, and Shamir had published their independent discovery.
In addition to the well-known RSA scheme, Rivest designed several other encoding methods for special applications. RC2, or �Ron�s Code 2,� was designed in 1987 as an encoding method for Lotus Corporation to use in the international version of their Lotus Notes product. The US National Security Agency (NSA) had prohibited the export of software unless it met restrictions designed to ensure that sensitive technology did not fall into unfriendly hands; RC2 was effective but still met those restrictions. Details of all six (two of which were never released) of Ron�s RC algorithms can be found here.
Rivest�s interests in security are not limited to encryption. For example, he is a member of the US government technical committee that develops election guidelines, and he published a 2006 paper [5] describing a novel three-ballot voting scheme. The paper is posted on his MIT website and is modified occasionally to eliminate problems that others have noted. As Rivest notes at the end:
ThreeBallot is hereby placed in the public domain�I am not filing for any patents on this approach, and we encourage others who work on extensions, improvements, or variations of this approach to act similarly. Our democracy is too important...
Ron is also an inspirational teacher. His co-written influential textbook Introduction to Algorithms [3], based on his undergraduate and graduate courses, has become a classroom standard. More than 500,000 copies were sold in 20 years. "




REFERENCES
==========

[1] Available: https://gist.github.com/davewongillies/7050080
[2] SMIME man page







(50 points) 2. A Merkle tree (hash tree) is a tree of hashes in which the leaves are hashes of data blocks
in, for instance, a file or set of files. Nodes further up in the tree are the hashes of their respective
children. For example, in the picture hash 0 is the result of hashing the result of concatenating hash 0-0
and hash 0-1. That is, hash 0 = hash( hash 0-0 + hash 0-1 ) where + denotes concatenation.
Merkle trees can be used to verify any kind of data stored, handled and transferred in and between
computers. Currently the main use of hash trees is to make sure that data blocks received from other
peers in a peer-to-peer network are received undamaged and unaltered, and even to check that the
other peers do not lie and send fake blocks. Suggestions have been made to use hash trees in trusted
computing systems.
Answer the following questions:
a) Give a specific scenario in which the Merkle tree is used to protect the integrity of the data and
explain how Merkle tree is used to protect the security of the message. (I have enclosed a paper
in which the Merkle tree is used to protect data security in wireless sensor networks. It is ok to
use the paper as an example to answer the question a) and explain how Merkle tree works.
However, you are always encouraged to look for other solutions using Merkle tree other than
the example given in the paper.)
b) For the same scenario, think about a single hash function solution, such as SHA-2. Can you
replace the Merkle tree using the single hash function in the scenario given in a)? Why or why
not?