# leet-day60

# Minimum Deletions to Make Character Frequencies Unique

This C++ solution solves the problem of finding the minimum number of character deletions required to make the frequencies of all characters unique in a given string `s`.

## Problem Description

A string `s` is called "good" if there are no two different characters in `s` that have the same frequency. The task is to determine the minimum number of characters you need to delete from `s` to make it "good."

### Example

Input: `s = "aaabbbcc"`
Output: `2`
Explanation: You can delete two 'b's resulting in the good string "aaabcc".

### Constraints

- `1 <= s.length <= 105`
- `s` contains only lowercase English letters.

## Approach

1. Create an array `freq` of size 26 (representing the 26 lowercase English letters) to store the frequency of each character in the string `s`.

2. Iterate through each character in `s` and update its frequency in the `freq` array.

3. Initialize a variable `ans` to keep track of the total number of characters to delete.

4. Iterate through the `freq` array and calculate the number of characters that need to be deleted to make the string "good." For each character with a frequency greater than 1, subtract one from its frequency and add that value to `ans`.

5. Return the value of `ans` as the minimum number of deletions needed.

## Usage

You can use the `minDeletions` function to find the minimum number of characters to delete for any given string. Here's how you can use it:

```cpp
Solution solution;
string s = "aaabbbcc";
int result = solution.minDeletions(s); // Should return 2
```

## Complexity Analysis

- Time Complexity: O(n), where n is the length of the input string `s`. The algorithm iterates through the string once to calculate the character frequencies.
- Space Complexity: O(1) since the `freq` array has a fixed size of 26, which is a constant.

