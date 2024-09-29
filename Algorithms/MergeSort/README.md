# Merge Sort

The Merge Sort algorithm is a divide-and-conquer algorithm that sorts an array by first breaking it down into smaller 
arrays, and then building the array back together the correct way so that it is sorted.

* **Divide:** The algorithm starts with breaking up the array into smaller and smaller pieces until one such sub-array only consists of one element.

* **Conquer:** The algorithm merges the small pieces of the array back together by putting the lowest values first, resulting in a sorted array.

### How it works:

1. Divide the unsorted array into two sub-arrays, half the size of the original.
2. Continue to divide the sub-arrays as long as the current piece of the array has more than one element.
3. Merge two sub-arrays together by always putting the lowest value first.
4. Keep merging until there are no sub-arrays left.

Take a look at the drawing below to see how Merge Sort works from a different perspective. As you can see, the array is 
split into smaller and smaller pieces until it is merged back together. And as the merging happens, values from each 
sub-array are compared so that the lowest value comes first.

<br>
<p align="center">
  <img src="https://www.w3schools.com/dsa/img_mergesort_long.png" alt="Merge Sort">
</p>

### Complexity

For a general explanation of what time complexity is, visit **[this page](https://www.w3schools.com/dsa/dsa_timecomplexity_theory.php)**.

The time complexity for Merge Sort is:

* **Best Case Complexity**: O(n log n)

And the time complexity is pretty much the same for different kinds of arrays. 
The algorithm needs to split the array and merge it back together whether it is already sorted or completely shuffled.

The image below shows the time complexity for Merge Sort.

<br>
<p align="center">
  <img src="https://www.w3schools.com/dsa/img_runtime_mergesort.png" alt="Merge Sort Time Complexity">
</p>

### Implementation

- **[MergeSort.py](MergeSort.ipynb)** - The main implementation of the Merge Sort algorithm in Python.
- **[MergeCount.ipynb](MergeCount.ipynb)** - An implementation of the Merge Sort algorithm that counts the number of inversions in an array.


