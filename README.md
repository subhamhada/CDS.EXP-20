# EXPERIMENT 20

### AIM
To study and implement Sorting Algorithm
1. Selection sort
2. Insertion sort
3. Bubble sort
   
### SOFTWARE USED
VS Code

### THEORY
In C++, sorting refers to the process of arranging elements in a specific order, typically in ascending or descending order. Sorting algorithms can be applied to arrays, vectors, or other containers to reorder the elements based on their values.<br>

1. *Selection Sort:*
* Selection Sort works by repeatedly finding the minimum element from the unsorted part of the array and swapping it with the first unsorted element.
* Time Complexity: O(n²) for all cases.
* Space Complexity: O(1) (in-place sorting). <br>
 
![insertionsort](https://github.com/user-attachments/assets/2ccc22cf-aad8-4dab-b130-3d13ebbf052b)

2. *Insertion Sort:*
* Insertion Sort works by building a sorted array one element at a time. It picks each element and inserts it into its correct position within the already sorted part of the array.
* Time Complexity: O(n²) in the worst case; O(n) in the best case (already sorted).
* Space Complexity: O(1) (in-place sorting). <br>
 

<img width="540" alt="Selection-sort-0" src="https://github.com/user-attachments/assets/6e076259-9846-4ad2-9bcf-b3ee157646f0">
<img width="540" alt="Selection-sort-1" src="https://github.com/user-attachments/assets/bfcb8590-f5ba-421c-8d48-2d2792c5d173">
<img width="540" alt="Selection-sort-2" src="https://github.com/user-attachments/assets/dd6035aa-bccd-4cc3-b3c7-e4d75117b91a">
<img width="540" alt="Selection-sort-3_1" src="https://github.com/user-attachments/assets/5a35c04b-a63a-4e55-8024-c224bf50983c">

3. *Bubble Sort:*
* Bubble Sort repeatedly swaps adjacent elements if they are in the wrong order. The largest element "bubbles up" to its correct position after each pass.
* Time Complexity: O(n²) in the worst case.
* Space Complexity: O(1) (in-place sorting). <br>
  
![bubble_sort](https://github.com/user-attachments/assets/e9802b59-1921-42ca-a244-dc3956c8f8e9)
 
### CODE & OUTPUT 
1. CODE A:
```
//subham
//entc B2
//23070123132
//experiment 20
#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void s_sort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;
    int arr[no_el];

    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    s_sort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    return 0;
}
```

* OUTPUT A: <BR>

2. CODE B:
```
//subham
//entc B2
//23070123132
//experiment 20
#include<iostream>
using namespace std;

void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        // Move elements of arr[0..i-1], that are greater than key, to one position ahead of their current position
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

int main() {
    int n;
    cout << "How many elements in your array?" << endl;
    cin >> n;
    
    int arr[n];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    insertionSort(arr, n);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    
    return 0;
}
```

* OUTPUT B: <BR>

3. CODE C:
```
//subham
//entc B2
//23070123132
//experiment 20
#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void bubbleSort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;

    int arr[no_el];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    bubbleSort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    return 0;
}
```
* OUTPUT C: <BR>


### CONCLUSION
These algorithms are primarily useful for educational purposes, and while they work well on small datasets, more advanced sorting algorithms such as Quick Sort, Merge Sort, or Heap Sort are generally preferred for large datasets due to their better performance
