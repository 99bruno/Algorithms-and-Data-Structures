# RSA

**RSA** (Rivest-Shamir-Adleman) is a public-key cryptosystem that is widely used for secure data transmission. 
It is also one of the oldest. The acronym RSA comes from the surnames of Ron Rivest, Adi Shamir, and Leonard Adleman, 
who first publicly described the algorithm in 1977.

### How it works:

RSA involves a public key and a private key. The public key can be known by everyone and is used for encrypting messages.

Messages encrypted using the public key can only be decrypted with the private key. The keys for the RSA algorithm are generated the following way:

1. Choose two distinct prime numbers p and q.
2. Compute n = p * q.
3. Compute the totient of n, φ(n) = (p-1) * (q-1).
4. Choose an integer e such that 1 < e < φ(n) and e is coprime to φ(n).
5. Compute the secret exponent d, such that (d * e) % φ(n) = 1.
6. The public key is (e, n) and the private key is (d, n).
7. To encrypt a message m, compute c = m^e % n.
8. To decrypt a message c, compute m = c^d % n.

### Complexity

The time complexity of the RSA algorithm is:

* **Best Case Complexity**: O(n^3)
* **Average Case Complexity**: O(n^3)
* **Worst Case Complexity**: O(n^3)

The time complexity for the RSA algorithm is O(n^3) because we are iterating through the entire number to calculate the encryption and decryption.

### Implementation

- **[RSA.ipynb](RSA.ipynb)** - The main implementation of the RSA algorithm in Python.