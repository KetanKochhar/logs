# Day 5 

### DBMS

- Inserting multiple records in SQL:
```sql
INSERT INTO table_name (column1, column2)  VALUES    (value1a, value2a),   (value1b, value2b),   (value1c, value2c);
```
- this command does not works in oracle apex so we use 
```sql
INSERT ALL 
INTO table_name (column1 , column2) VALUES (value1a , value1b)
INTO table_name (column1 , column2) VALUES (value1b , value2b)
SELECT 1 FROM DUAL ;
```
- In this command last `select 1 from dual` is important to push only one row to the table
###  IIMUN Meeting

-  International trip after qualifying general aptitude test.
-  Fee: ₹4.5 lakhs.
-  Check eligibility and ROI before applying.



### **Data Structures**

###  Topic: **Time Complexity**

---

## 1. **Time and Space Complexity**

- **Time Complexity:**  
    Measures how the runtime of an algorithm changes with the size of input `n`.  
    It gives a high-level understanding of an algorithm’s efficiency.
    
- **Space Complexity:**  
    Refers to the amount of memory (RAM) required by the algorithm to run to completion.  
    This includes input size, auxiliary space, and call stack (for recursion).
    

---

##  2. **Asymptotic Notations**

Used to describe the **growth of an algorithm** as input size becomes large:

| Notation            | Meaning         | Definition                  |
| ------------------- | --------------- | --------------------------- |
| **Big O** – O(f(n)) | **Upper bound** | Worst-case scenario         |
| **Omega** – Ω(f(n)) | **Lower bound** | Best-case scenario          |
| **Theta** – Θ(f(n)) | **Tight bound** | Average-case (exact growth) |

### Examples:

- `O(n)`: Algorithm takes at most linear time.
- `Ω(1)`: Algorithm takes at least constant time.
- `Θ(n²)`: Algorithm takes quadratic time in all cases.

---

## 3. **Example**
### Problem:

Find the relationship between  
**`4n²` and `O(n³)`**

### Solution:

- We need to check if: `4n² = O(n³)`
    
- **Big O is an upper bound**, so we ask:  
    Is there a constant `c` and `n₀` such that:  
    `4n² ≤ c·n³` for all `n ≥ n₀`?
    Yes — because `n³` grows faster than `n²`.  
    So, `4n² = O(n³)` is **True** 
- theroritacial solution 
	- f(n) = $4n^2$
	- g(n) = $n^3$
	- 0 < f(n) $\leq$ c . g(n)
	- 0 < $4n^2$ $\leq$ c . $n^3$  (dividing both the sides with $n^2$)
	- 0 < $4$ $\leq$ c . $n$ 
	- 0 < $\frac{4}{n}$ $\leq$ c ------- equation number 1
	- if $n=1$ 
		- then max value for c will be 4
	- $c = 4$
	- putting value of c in equation 1 
	-  $0 <\frac{4}{N_0} \leq 4$ 
	- $0 < 4 \leq {4}{N_0}$ 4
	- $0 < \frac{4}{4} \leq N_0$
	- $0 < 1 \leq N_0$
	- By solving this we got
		- $N_0 = 1$
	- By calculating $N_0$ & $c$
	- f(n) $\leq$ 4g(n),$\forall$ n $\leq$ 1
    

---

## **Different functions**

We were asked to **find the relationship** between different time complexities:

###  Ordered from slowest to fastest growth:

```
1 < log(n) < n < n·log(n) < n² < n³ < 2ⁿ < n!
```

### Key Concept:

If `f(n)` grows slower than `g(n)`, then:
**f(n) = O(g(n))**

### Relationships:

- `1 = O(log n)`  
- `log n = O(n)`
- `n = O(n log n)`
- `n log n = O(n²)`
- `n² = O(n³)`
- `n³ = O(2ⁿ)`

---
