## Two Sum

🔗 Problem: https://leetcode.com/problems/two-sum/

### 🔍 Pattern
- Hashing
- Lookup while iterating

### 🧠 Logic
- Store number → index in HashMap
- For each number, check if `target - num` exists
- If yes, return indices

### 🚀 Approach
1. Initialize HashMap
2. Loop through array
3. Check complement
4. Insert current element

### ⏱️ Time & Space
- Time: O(n)
- Space: O(n)

### ⚠️ Mistakes / Edge Cases
- Don't insert before checking
- Works only if exactly one solution exists

### 💡 Key Insight
- Trading space for time using HashMap


## 🧪 Example Walkthrough

**Input:**
```
nums = 
target = 9
```

### Step-by-step Execution

| Step | Current Number | Complement (target - num) | HashMap (value → index) | Result |
|------|----------------|---------------------------|--------------------------|---------|
| 1 | 2 (index 0) | 7 | `{}` | 7 not found → insert (2 → 0) |
| 2 | 7 (index 1) | 2 | `{2 → 0}` | 2 found → return [0, 1] |

**Output:**
```
[0, 1]
```

---

## 🔎 Why This Works

- HashMap allows **O(1)** lookup.  
- Each number is checked only once.  
- Complement lookup happens **before insertion**, preventing reuse of the same element.

---

## 🧠 Visual Insight

```
target = 9

2  → need 7  ❌
7  → need 2  ✅ (found in map)
```

---

## 📌 Final Takeaway

- Always **check first, insert later**.  
- Best example of a **space–time tradeoff**.  
- A classic **hashing pattern** problem.  
```
