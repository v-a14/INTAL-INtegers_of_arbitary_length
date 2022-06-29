char* intal_add(const char* intal1, const char* intal2)
    • Compare both intals, pass the larger intal as intal1 to the helper function intal_adder. 
    • intal_add creates a new char pointer size of larger intal + 2
    • add characters from the back of the array to the front
    • remove any leading zeros using removeLeadZero
    • return to intal_add
int intal_compare(const char* intal1, const char* intal2)
    • Compare both char arrays first length wise.
    • If length of intal1 is greater return 1, if length of intal2 is greater return -1
    • if length are same return 1 or -1 based on which character is greater.
    • Return 0 otherwise
char* intal_diff(const char* intal1, const char* intal2)
    • Return difference of 2 intals. Pass the larger intal as intal1 to the helper function intal_differ
    • intal_diff creates a new char pointer with space of larger intal + 2
    • repeatedly subtarct characters. Borrow digit if required.
    • Remove any leading zeros using removeLeadZero
    • return to intal_differ
char* intal_multiply(const char* intal1, const char* intal2)
    • Check for edge cases
    • Create a new char pointer with space of sum of length of both intals
    • Pass to helper function intal_multy
    • multiply each character by character
    • add any remaining carry
    • return to intal_multiply
    • remove lead zeros using removeLeadZero
char* intal_mod(const char* intal1, const char* intal2)
    • check for edge cases
    • check lengths of numerator and denominator
    • create a copy of numerator
    • equalise length if required by multiplying with zeros to denominator
    • repeatedly subtract till numerator less than new denominator
    • repeat the process till numerator is less than denominator
char* intal_pow(const char* intal1, unsigned int n)
    • if n is zero return 1
    • if n is odd, multiply intal by itself by odd power 
    • if n is even multiply intal by itself by even power
    • continue till n is reached

char* intal_gcd(const char* intal1, const char* intal2)
    • check edge cases
    • if not edge cases, find intal1 mod intal2
    • find gcd of intal2, result of intal1 mod intal2
char* intal_fibonacci(unsigned int n)
    • check for edge cases
    • create 3 char pointers, initial pointer values are ‘0’ and ‘1’
    • iterate through 2 to n, use the formula f(n) = f(n-1) + f(n-2) to determine the next fibonacci value
char* intal_factorial(unsigned int n)
    • check for edge cases
    • create char pointer to intal “1”
    • till loop does not reach n, increment by “1” and multiply result with another char pointer result
char* intal_bincoeff(unsigned int n, unsigned int k)
    • Check for edge cases
    • create a pointer of char pointers, of size k
    • use dynamic programing to find value of c(n,k). 
    • fill in the value of the table
    • copy the value of last element to another pointer
    • free the table
int intal_max(char **arr, int n)
    • assign index of max value as the zeroth element of the array
    • startin from index 1 to (n-1), compare the max value
    • if greater than max value, remember the position of the element
    • return position of max value
int intal_min(char **arr, int n)
    • assign the zeroth index as the minimum element
    • loop through array index i to (n-1), compare to min value
    • if less than min value, update the variable
    • return variable
int intal_search(char **arr, int n, const char* key)
    • compare each element of array with the key
    • if intal_compare(arr[i],key) == 0, return i
int intal_binsearch(char **arr, int n, const char* key)
    • assign value lo as zero and high as n-1
    • while value of lo is less than hi, do 
        ◦ find mid element
        ◦ compare mid element to key
        ◦ if mid element is key return mid index
        ◦ if mid element is less than key search the higher half of array
        ◦ else search lower half of array
        ◦ return -1 if loop is not terminated by return statement
void intal_sort(char **arr, int n)
    • implement the merge sort function
    • No usage of auxillary stack because iterative
    • calculate left, middle and right bound. Pass to helper function merge at each loop
    • create temprorary arrays with elements to left and right separately
    • at each iteration, compare left and right element,add the smaller value back to the list
    • continue till either list empties
    • add remaining elements back to array
    • keep repeating till left bound is the last element.

char* coin_row_problem(char **arr, int n)
    • assign 3 char pointers prev to ‘0’, curr to zeroth element of array, next to ‘0’
    • iterate through the whole array
    • value of next is max(prev+arr[i], curr)
    • if prev not equal to curr
        ◦ free prev
        ◦ prev is now curr
    • curr is now next
    • free prev if prev not equal curr
    • return curr
