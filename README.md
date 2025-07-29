# Decode String

## Problem Description

You are given an **encoded string** `s`. Return its **decoded version**.

### Encoding Rule:
- The format is: `k[encoded_string]`
  - `k` is a **positive integer**.
  - The substring inside `[]` is repeated **exactly `k` times**.
  - Nested encodings are allowed.

> Note:
> - All input strings are **valid**.
> - Digits are used **only** for `k` (repeat count).
> - No letters or brackets will appear inside the digits (e.g., no input like `3a` or `2[4]`).

---

## Examples

### Example 1:

**Input:**  
`s = "3[a]2[bc]"`  
**Output:**  
`"aaabcbc"`  

**Explanation:**
- `"3[a]"` → `"aaa"`
- `"2[bc]"` → `"bcbc"`
- Final: `"aaabcbc"`

---

### Example 2:

**Input:**  
`s = "3[a2[c]]"`  
**Output:**  
`"accaccacc"`  

**Explanation:**
- `"a2[c]"` → `"acc"`
- `"3[acc]"` → `"accaccacc"`

---

### Example 3:

**Input:**  
`s = "2[abc]3[cd]ef"`  
**Output:**  
`"abcabccdcdcdef"`  

**Explanation:**
- `"2[abc]"` → `"abcabc"`
- `"3[cd]"` → `"cdcdcd"`
- Final: `"abcabccdcdcdef"`

---

## Constraints

- `1 <= s.length <= 30`
- `s` consists of:
  - Lowercase English letters,
  - Digits,
  - Square brackets `[` and `]`.
- The input is **well-formed** and **guaranteed valid**.
- All integers for `k` are in range `[1, 300]`.
- The **length of decoded string** will **not exceed 10⁵**.
