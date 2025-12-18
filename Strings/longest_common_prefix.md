## Longest Common Prefix

🔗 Problem: https://leetcode.com/problems/longest-common-prefix/

---

### 🔍 Pattern
- Prefix comparison
- String trimming
- Horizontal scanning

---

### 🧠 Logic
- Assume the first string is the prefix.
- Compare this prefix with every other string.
- If the current string does not start with the prefix, shorten the prefix.
- Continue until the prefix matches or becomes empty.

---

### 🚀 Approach
1. Take the first string as the initial prefix.
2. Iterate through remaining strings.
3. While the string does not start with the prefix:
   - Remove the last character from prefix.
4. If prefix becomes empty, return `""`.
5. Return the final prefix.

---

### ⏱️ Time & Space
- **Time Complexity:** O(n × m)  
  where `n` = number of strings, `m` = length of prefix
- **Space Complexity:** O(1) (no extra space used)

---

### 🧪 Example Walkthrough

#### Example 1
```text
Input: ["flower", "flow", "flight"]

## Step-by-step

| Step | Prefix | Current Word | Result |
|------|---------|---------------|---------|
| Start | "flower" | — | Initial prefix |
| 1 | "flower" | "flow" | Not matching → shorten |
| 2 | "flow" | "flow" | Match |
| 3 | "flow" | "flight" | Not matching → shorten |
| 4 | "fl" | "flight" | Match |

**Output:**
```
"fl"
```

---

## Example 2

**Input:**
```
["dog", "racecar", "car"]
```

| Step | Prefix | Current Word | Result |
|------|---------|---------------|---------|
| Start | "dog" | — | Initial prefix |
| 1 | "dog" | "racecar" | No match → shorten |
| 2 | "" | — | Prefix empty |

**Output:**
```
""
```

---

## ⚠️ Edge Cases

- Array contains an empty string → return `""`  
- Only one string → return that string  
- No common prefix → return `""`  
```
