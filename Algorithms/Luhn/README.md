# Luhn

**The Luhn algorithm**, also known as the modulus 10 or mod 10 algorithm, is a simple checksum formula used to validate a 
variety of identification numbers, such as credit card numbers, IMEI numbers, Canadian Social Insurance Numbers. 
The LUHN formula was created in the late 1960s by a group of mathematicians. 
Shortly thereafter, credit card companies adopted it. Because the algorithm is in the public domain, 
it can be used by anyone. Most credit cards and many government identification numbers use the algorithm as a simple 
method of distinguishing valid numbers from mistyped or otherwise incorrect numbers. It was designed to protect 
against accidental errors, not malicious attacks

### How it works:

Consider the example of an account number '79927398713'. 

1. Starting from the rightmost digit, double the value of every second digit, 

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/gfgedit-300x60.png" alt="Merge Sort">
</p>

2. If doubling of a number of results in a two-digit number i.e. greater than 9(e.g., 6 × 2 = 12), then add the digits of the product (e.g., 12: 1 + 2 = 3, 15: 1 + 5 = 6), to get a single digit number.

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/gfg3-3-300x81.png" alt="Merge Sort">
</p>

3. Now take the sum of all the digits.

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/gfg1-1-300x81.png" alt="Merge Sort">
</p>

4. If the total modulo 10 is equal to 0 (if the total ends in zero) then the number is valid according to the Luhn formula; else it is not valid.
 
<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/gfg2-2-300x101.png" alt="Merge Sort">
</p>

**Since the sum is 70 which is a multiple of 10, the account number is possibly valid.** 

The idea is simple; we traverse from the end. For every second digit, we double it before adding it. We add two digits of the number obtained after doubling.  

### Complexity

The time complexity for the Luhn algorithm is:

* **Best Case Complexity**: O(n)

The time complexity for the Luhn algorithm is O(n) because we are iterating through the entire number to calculate the checksum.

### Implementation

- **[Luhn.ipynb](Luhn.ipynb)** - The main implementation of the Luhn algorithm in Python.
- **[MissedValuesLuhn.ipynb](MissedValuesLuhn.ipynb)** - An implementation of the Luhn algorithm that calculates the missing values in a credit card number.