# System Design - CheatSheet

A compilation of notes that I made when learning these programming topics online - Note a majority of the content and code was taken off of 
online websites so I do not take any ownership of the below. The following is simply notes compiled for learning purposes.


## Getting Started

Currently AlgorithmsDataStructures-CheatSheet contains various text files for notes but is primarily composed of this README file which supports the markdown formatting language. This makes the notes and code look a lot better and supports many awesome features like quick links 
and makes formatting much easier. 


### Prerequisites

In the future I might add a html document which also performs some formatting and if that comes out, ideally the html and css
would be written for web browsers on large screens which support the newest version of bootstrap and html 5.
I use the following application when building and testing html.

```
Chrome Version 71.0.3578.98
```


## Built With

* [Markdown](https://guides.github.com/features/mastering-markdown/) - Syntax styling



## Authors

* **Lichen Ma** - *compiling information* 



## Acknowledgments

* **content belongs to respective creators**


### Algorithms 
1. [Dynamic Programming](#dynamicProgramming)
    * [Fibonacci Numbers](#dynamicProgrammingFibonacciNumbers)
2. [Sorting](#sorting)
    * [Bucket Sort](#sortingBucketSort)
    * [Bubble Sort](#sortingBubbleSort)
    * [Insertion Sort](#sortingInsertionSort)
    * [Selection Sort](#sortingSelectionSort)
    * [Heap Sort](#sortingHeapSort)
    * [Merge Sort](#sortingMergeSort)
3. [Comparator](#comparator)




### Data Structures 
1. [Trie](#trie)



# Algorithms 

<br><br><br>
***
<a name="dynamicProgramming"></a>
# Dynamic Programming 


Dynamic Programming is mainly an optimization over plain recursion. Whenever we see a recursive 
solution that has repeated calls for the same inputs we can optimize it using Dynamic Programming. The
idea is to simply store the results of the subproblems so that we do not have to re-compute them when
needed later. This simple optimization reduces time complexities from exponential to polynomial. For 
example, if we write the simple recursive solution for Fibonacci numbers, we get exponential time 
complexity and if we optimize it by storing solutions of subproblems time complexity reduces to linear.

We break a complex problem up into a collection of simpler subproblems and solve each of those 
subproblems just once and storing their solutions using a memory-based data structure. 





<br><br>
<a name="dynamicProgrammingFibonacciNumbers"></a>
## Fibonacci Numbers 

<br><br>
### Approach 1: Recursion

```java 
class fibonacci {
	static int fib(int n) {
		if (n<=1){
			return n;
		}
		return fib(n-1) + fib(n-2);
	}
