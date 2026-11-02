# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:

Python with NumPy and SciPy libraries, Google Colab.

## PROGRAM: 
```
# Huffman and Shannon-Fano Coding
import numpy as np
import math 

L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples: "))

for i in range(n): 
    pr = float(input(f"Enter the probability of sample {i + 1}: "))  
    p.append(pr)

for j in range(n): 
    l = float(input(f"Enter the length of sample {j + 1}: "))  
    lk.append(l)

# Average Codeword Length
for k in range(n):
    Avg1 = p[k] * lk[k]
    L += Avg1

# Entropy Calculation
for k in range(n):
    e = p[k] * math.log(1 / p[k], 2)
    hs += e
hs = round(hs, 3)

# Efficiency Calculation
eff = round(hs / L, 3)

# Redundancy Calculation
red = round(1 - eff, 3)

# Variance Calculation
var = 0
for k in range(n):
    var1 = p[k] * (lk[k] - L) ** 2
    var += var1
var = round(var, 3)

print(f"Average Codeword Length: {L}")
print(f"Entropy: {hs}")
print(f"Efficiency: {eff}")
print(f"Redundancy: {red}")
print(f"Variance: {var}")

```
## CALCULATION: 

![WhatsApp Image 2025-09-29 at 8 32 22 AM](https://github.com/user-attachments/assets/5e3a6e4c-8671-4912-bd64-cd9f0c6fe07d)


![WhatsApp Image 2025-09-29 at 8 32 47 AM](https://github.com/user-attachments/assets/dd4ea952-8d5a-4bbf-820b-c162807cbdd4)


![WhatsApp Image 2025-09-29 at 8 33 08 AM](https://github.com/user-attachments/assets/ca4a2c9a-ce40-4da8-810a-9f544ce483fb)


## OUTPUT:

<img width="468" height="454" alt="image" src="https://github.com/user-attachments/assets/8520adb5-808a-48cc-b22e-5c40a55293b2" />

## RESULTS: 
 The Huffman and Shannon-Fano coding techniques have been successfully applied to the given source. The average codeword length, entropy, variance, redundancy, and efficiency have been computed.
