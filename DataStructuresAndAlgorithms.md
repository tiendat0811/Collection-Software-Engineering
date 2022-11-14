# Data structures and Algorithms

## Data Type

- Primitive Value: store value
- Reference Value: store address
- What's the difference between primitive and reference value?

Primitive Value: The values of two variables are independent. Changing the value of one variable will not affect the other
Ex:

```
let a = 1
let b = a
b = b + 1
console.log(a + '-' + b) //--> 1 - 2
```

Reference Value: When assigning or copying values, save the memory address. If one variable changes in value, the other variable will also be changed.
Ex:

```
const television = {
	isOn = false
}
light = television
televison.isOn = true
console.log(light.isOn) //--> true
```

## Data structures

- Array
  - What is array?
  - An Array is a collection of elements, a elements of which are identified by an index (index)
  - All elements have the same data type
  - An array has a fixed size
  - Why is array used?
  - Use array whenever you want to create and store a list of multiple items in a variable. arrays is especially useful when creating an ordered collection (index) for quick access if its order is known
  - Elements have same data type
  - What are the advantage and disadvantage of an array?
  - Advantage:
    - Arrays store multiple data of similar types with the same name
    - It allows random access to elements
    - As the array is of fixed size and stored in contiguous memory locations there is no memory shortage or overflow
  - Disadvantage:
    - The size of the array should be known in advance
    - The array is a static data structure with a fixed size so, the size of the array cannot be modified further and hence no modification can be done during runtime
    - Insertion and deletion operations are costly in arrays as elements are stored in contiguous memory
    - If the size of the declared array is more than the required size then, it can lead to memory wastage
- Map
  - What is Map?
  - A map data structure is a data structure that maps a key (key) to the value of that key (called value)
  - In this data structure, each key will receive a different value
  - Why is Map used?
  - Map data type is ideal to use in look-up type situations where there is an identifying value and an actual value that is represented by the identifying value
  - Map tends to perform better in storing large data sets, especially when the keys are unknown
  - What are the advantage and disadvantage of Map?
  - Advantage:
    - Retaining the insertion order is a big advantage of a Map, as a Map will maintain the order of entries
    - In a Map, there is more flexibility with key values, as a key can be any value such as functions, objects, and primitives
    - Map include the size property, an easy way to get the number of items in the Map
    - Performance of frequent additions or even removals of key-value pairs is better
  - Disadvantage:
    - No direct compatibility with JSON
    - Takes a long time to initialize
    - Map mainly useful when supporting data structures for objects and arrays.
- Set

  - What is Set?
  - Set is a type of data structure used to store elements that are not duplicated and sorted in ascending or descending order
  - Why is Set used?
  - Because set contains only elements that do not overlap, set is used in cases where the data does not overlap, such as employee IDs, primary keys
  - Set are used to determine the distinct values in an array
  - Set are used to detect cycles in a Linked List
  - Sets are used in various database operations such as performing joins
  - What are the advantage and disadvantage of Set?
  - Advantage:
    - Set can be used to store unique values in order to avoid duplications of elements present in the set
    - Elements in a set are stored in a sorted fashion which makes it efficient
    - Set are dynamic, so there is no error of overflowing of the set
    - Searching operation takes O(logN) time complexity
  - Disadvantage:
    - Elements in a set can only be accessed with pointers, there is no indexing in set like arrays
    - Set is very complex to implement because of its structure and properties
    - A set takes O(logN) time complexity for basic operations like insertion and deletion

- What's the difference between `Array` and `Linked List`?

| Compare | Array | Linked List |
| ----------- | ----------- | |------------ |
| Basic | Is a fixed set of elements | A large set of data arranged in some order|
| Size | Fixed, defined at declaration | It doesn't need to be defined |
|Sort order | Stored consecutively | Randomly stored |
|How to access | Direct or random | Sequential access|
|Insert and delete elements | Relatively slow due to the need to shift the array | Easy, fast and convenient |
| Search |Binary search and linear search |Linear Search |
| Memory | Low| Medium |

- What's the difference between `Array` and `Map`?

| Compare | Array | Map |
| ----------- | ----------- | |------------ |
| Basic | Is a fixed set of elements | Is a data structure that maps a key (key) to the value of that key (called value)|
| Size | Fixed, defined at declaration | It doesn't need to be defined |
|Sort order | Stored consecutively | Randomly stored |
|How to access | Direct or random | Direct access|
|Insert and delete elements | Relatively slow due to the need to shift the array | Easy, fast and convenient |
| Search |Binary search and linear search |Linear Search |
| Memory | Low| High |

- What's the difference between `Array` and `Set`?

| Compare | Array | Set |
| ----------- | ----------- | |------------ |
| Basic | Is a fixed set of elements | Is a type of data structure used to store elements that are not duplicated and sorted in ascending or descending order|
| Size | Fixed, defined at declaration | It doesn't need to be defined |
| Store | Can duplicate| Only one value (=== compare) |

### Algorithms

- Algorithm complexity

  - What is time complexity so important?
    Time complexity is **defined as the amount of time taken by an algorithm to run**, as a function of the length of the input. It measures the time taken to execute each statement of code in an algorithm. It is not going to examine the total execution time of an algorithm. Rather, it is going to give **information about the variation (increase or decrease) in execution time** when the number of operations (increase or decrease) in an algorithm.
  - What is algorithm complexity?
    Algorithm complexity is a relative quantity representing the number of operations of an algorithm compared to the size of the input (n).
    Ex: The average space complexity of Quick Sort is O(log n) and the worst case space complexity is O(n)

- Sort

  - Quicksort
    - Time Complexity: Average O(n log n)
    - Worst: O(n2)
    - Data Complexity: Varies depending on implementation
    - Optimal: Occasionally
    - **Choose pivot:**
    - first or last element
    - middle element
    - random element (not recommend)
    - median of the first, last and middle

Example:

```
const quickSort = (arr) => {
    if(arr.length < 2) return arr;
    // choose last element is pivot
    const pivotIndex = arr.length - 1;
    const pivot = arr[pivotIndex];
    const left = [];
    const right = [];

    let currentItem;
    for(let i = 0; i < pivotIndex; i++) {
        currentItem = arr[i];

        if(currentItem < pivot) {
            left.push(currentItem);
        } else {
            right.push(currentItem);
        }
    }

    return [...quickSort(left), pivot, ...quickSort(right)];
}

console.log(quickSort([100, 2, 5, 4, 7, 5, 6, 8, 0, 12, 34, 15]));
// *** => [0, 2, 4, 5, 5, 6, 7, 8, 12, 15, 34, 100]
```

- Search
  - What are the advantage and disadvantage of search algorithms?
    Binary search
  - Advantage:
    - It is better than a linear search algorithm since its run time complexity is O(logN)
    - At each iteration, the binary search algorithm eliminates half of the list and significantly reduces the search space
    - The binary search algorithm works even when the array is rotated by some position and finds the target element
  - Disadvantage:
    - The recursive method uses stack space
    - Binary search is error-prone
    - Caching is poor
