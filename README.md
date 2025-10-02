# LEETCODE-Maths-3100

### Input:

`numBottles = 13, numExchange = 6`

---

### Dry Run Step by Step

**Initial state:**

* `numBottles = 13`
* `empty = 0`
* `drunk = 0`
* `numExchange = 6`

---

#### Iteration 1:

* `empty += 13 → empty = 13`
* `drunk += 13 → drunk = 13`
* `numBottles = 0`

Check exchange:

* `empty (13) >= numExchange (6)` ✅

  * `numBottles += 1 → numBottles = 1`
  * `empty -= 6 → empty = 7`
  * `numExchange += 1 → numExchange = 7`

**State after Iter 1:**

* `numBottles = 1`, `empty = 7`, `drunk = 13`, `numExchange = 7`

---

#### Iteration 2:

* `empty += 1 → empty = 8`
* `drunk += 1 → drunk = 14`
* `numBottles = 0`

Check exchange:

* `empty (8) >= numExchange (7)` ✅

  * `numBottles = 1`
  * `empty -= 7 → empty = 1`
  * `numExchange += 1 → numExchange = 8`

**State after Iter 2:**

* `numBottles = 1`, `empty = 1`, `drunk = 14`, `numExchange = 8`

---

#### Iteration 3:

* `empty += 1 → empty = 2`
* `drunk += 1 → drunk = 15`
* `numBottles = 0`

Check exchange:

* `empty (2) >= numExchange (8)` ❌ no exchange

**State after Iter 3:**

* `numBottles = 0`, `empty = 2`, `drunk = 15`, `numExchange = 8`

---

### Loop Ends

Because `numBottles == 0` and no more exchange is possible.

---

### ✅ Final Result:

`drunk = 15`

---
