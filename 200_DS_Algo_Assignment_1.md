## Data Structures Assignment 1 [115 points]

Warm-up time. This is a prereq to any serious coding.

Deliverable: Answers to questions & C# (or Java) and C++ programs.

# Background Reading

## Abstract Data Types

Note: An "associative array" is not a conventional array. We'll interchangeably use the terms `map` and `dictionary` instead.

Grok the following articles & answer the following questions.

### [Reading 1] Arrays [25 points]
Skim these articles:

- JavaScript https://www.w3schools.com/js/js_arrays.asp
- C# https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/arrays/ 
- C++ http://www.cplusplus.com/doc/tutorial/arrays/
- Big-O https://web.archive.org/web/20181020210828/http://www.bigocheatsheet.com:80/
- Big-O of JavaScript Arrays https://stackoverflow.com/questions/11514308/big-o-of-javascript-arrays

**Question 1a: How do you initialize an array A of sequence 10, 20, 30 in JavaScript, C#, and C++? [5 points]**  
**Question 1b: Referring to Q1a, what does A[123] do in JavaScript, C#, and C++? What mechanisms cause these behaviours? [5 points]**  
**Question 1c: Why is the time complexity of APPENDING to the end of an array O(N) in C#/C++? [5 points]**  
**Question 1d: Referring to Q1c, why might this be different in JavaScript? [5 points]**  
**Question 1e: How are arrays represented differently in C# vs C/C++? (How are they referenced, what runtime support does C# provide & how?) [5 points]**  

### [Reading 2] Array-Lists [25 points]
Skim this article:

- Array versus List<T>: When to use which? https://stackoverflow.com/questions/434761/array-versus-listt-when-to-use-which

**Question 2a: When might one use an array over an arraylist in low-level code? (think: graphics, networking, file IO) [5 points]**  
**Program 1: Provide C# & C++ code for an ArrayList<T> with these 6 operations. Test your operations (~50 LOC C#, ~50 LOC C++) [20 points]**  

- new(capacity: int): ArrayList<T>
- length(): int
- append(item: T): void
- get(index: int): T
- clear(): void
- removeAt(index: int)

### [Reading 3] Linked Lists (& CPU caching) [15 points]
Skim these links (pun intended):

- https://www.interviewbit.com/courses/programming/topics/linked-lists/
- https://stackoverflow.com/questions/393556/when-to-use-a-linked-list-over-an-array-array-list?noredirect=1&lq=1
- https://stackoverflow.com/questions/12065774/why-does-cache-locality-matter-for-array-performance
- https://www.quora.com/Why-arrays-have-better-cache-locality-than-linked-list

**Question 3a: `cons` constructs an object holding two parameters. Diagram the linked list formed by `(cons 1 (cons 2 (cons 3 nil)))`. [5 points]** 
- Note: (operation param1 param2) is known as Prefix Notation aka Polish Notation. https://en.wikipedia.org/wiki/Polish_notation#Computer_programming
- For example (+ 2 3) evaluates to 5 in Prefix Notation systems (e.g. LISP). Note C#, C++, JavaScript, and Python do not support prefix notation.
- Likewise, 2 3 * 5 + in reverse polish notation evaluates to (2 * 3) + 5 = 11. Fun fact, C# compiles down to something like this (discussed in future section).

**Question 3b: In C#, implement a class and Cons in <10 lines of code. Then, traverse Cons(1, Cons(2, Cons(3, null))) and print to console. [10 points]**

### [Reading 4] Unordered Maps (Aka Dictionaries, HashTables, HashMaps). [50 points]
Skim these links:
- https://stackoverflow.com/questions/2592043/what-is-a-hash-map-in-programming-and-where-can-it-be-used
- https://en.wikipedia.org/wiki/Hash_table
- https://stackoverflow.com/questions/2556142/chained-hash-tables-vs-open-addressed-hash-tables

**Question 4a: Describe how a separate-chaining-based hashmap works. [5 points]**  
**Question 4b: Describe how a linearly-probed openly-addressed hashmap works. [5 points]**  
**Question 4c: Why is quadratic probing often preferable over linear probing? [5 points]**  
**Question 4d: What is double hashing? How might it improve performance of open addressing over quadratic probing? [5 points]**  
**Question 4e: How might one implement a hashset leveraging a hashmap? [5 points]**  

**Implement a separate-chaining-based hashmap in C# or C++ with the following operations: [10 points]**

- new(): HashMap<TKey, TValue>
- add(k: TKey, v: TValue): void
- remove(k: TKey): bool // retval: whether removed
- contains(k: TKey): bool
- get(k: TKey): TValue
- keys(): TKey[]

**Implement a open-addressing-based hashmap in C# or C++ with the same operations as above [15 points]**
