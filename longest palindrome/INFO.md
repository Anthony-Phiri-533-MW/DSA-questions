# Longest Palindromic Substring

## Problem Description

Given a string `s`, return the **longest palindromic substring** in `s`.

A **palindrome** is a string that reads the same forward and backward.

### Examples

* **Input:** `s = "babad"`

  **Output:** `"bab"`
  *("aba" is also a valid answer)*

* **Input:** `s = "cbbd"`
  **Output:** `"bb"`

### Constraints

* `1 <= s.length <= 1000`
* `s` consists of only digits and English letters

---

## Approach / Intuition

The key idea is to **expand around possible centers** of a palindrome.

Every palindrome can be formed by expanding from:

* **A single center** (odd-length palindromes, e.g., `"aba"`)
* **Two adjacent centers** (even-length palindromes, e.g., `"abba"`)

### Steps:

1. Iterate through each index in the string.
2. Treat each index as the center of an odd-length palindrome.
3. Treat each index and the next index as the center of an even-length palindrome.
4. Expand outward while the characters match.
5. Track the longest palindromic substring found.

This avoids checking all substrings explicitly and efficiently finds the solution.

---

## Time Complexity

**O(n²)**

* There are `n` possible centers.
* For each center, expansion may take up to `O(n)` time.

---

## Space Complexity

**O(1)**

* Only constant extra space is used.
* No additional data structures are required.

---

This approach is optimal and commonly accepted for strings of length up to 1000.
