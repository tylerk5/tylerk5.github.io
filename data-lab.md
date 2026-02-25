---
layout: default
title: CS:APP Data Lab Breakdown
---

# Project: Integer Representation & Bit Manipulation

In this project, I completed the famous **CS:APP Data Lab**. The goal was to implement a set of functions that perform complex logical and arithmetic operations using a very limited subset of the C programming language.

## The Constraints
This wasn't typical coding. To prove a deep understanding of how computers handle data at the hardware level, I was forbidden from using:
* `if`, `else`, `while`, or `for` loops
* Casting or macros
* Large constants (nothing bigger than 0xFF)
* Standard arithmetic like `-` (in most cases)

## Highlight: The "Bit-Smearing" Technique
One of the most challenging functions was `greatestBitPos(int x)`, which returns a mask marking the position of the most significant bit.

### The Problem
Without a loop, you can't just "scan" from left to right to find the first `1`. 

### My Solution
I implemented an **OR-shifting** algorithm (also known as bit-smearing). By shifting the bits right and OR-ing them with the original value, I "smeared" the highest `1` all the way to the right. 

**Example:**
* **Initial:** `00010000`
* **Step 1 (shift 1):** `00011000`
* **Step 2 (shift 2):** `00011110`
* **Step 3 (shift 4...):** `00011111`

Finally, by using `mask & ~(mask >> 1)`, I was able to isolate just that original highest bit.



## Key Takeaways
* **De Morgan's Laws:** Used extensively to convert between AND/OR logic when specific operators were restricted.
* **Two's Complement:** Deepened my understanding of how negative numbers are stored and how arithmetic right-shifts preserve the sign bit.
* **Efficiency:** Every operation had a "cost" or a limit. I had to find the most mathematically "cheap" way to get the result.

---
*Note: Full source code is kept in a private repository to maintain academic integrity. Feel free to reach out if you'd like to discuss the logic further!*
---

<div style="margin-top: 50px; text-align: center;">
  <a href="./" class="btn" style="background-color: #0366d6; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold;">
    ← Back to Home
  </a>
</div>
