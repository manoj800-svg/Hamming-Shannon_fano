# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
Python IDE with
-> numpy library
-> math library
# Program:
```import math
p = [0.55, 0.15, 0.15, 0.1, 0.05]
lk = [2, 2, 2, 3, 3]
n = len(p)
L = sum(p[k] * lk[k] for k in range(n))
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)
eff = round(hs / L, 3)
red = round(1 - eff, 3)
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```

# Calculation:
![WhatsApp Image 2025-09-16 at 23 08 41_25de5aaf](https://github.com/user-attachments/assets/53557990-cd59-4eb6-95df-a824c4993575)

![WhatsApp Image 2025-09-16 at 23 09 04_7661f244](https://github.com/user-attachments/assets/2bbb6891-7bb5-4cca-bdf8-5ab38e14cf4e)

![WhatsApp Image 2025-09-16 at 23 09 41_e30fe6a9](https://github.com/user-attachments/assets/736ec652-c998-4645-8ec4-3d9d648d9ab3)
# Output
Average Codeword Length is : 2.1500000000000004

Entropy is : 1.844

Efficiency is : 85.8%

Redundancy is : 0.142

Variance is : 0.128

# Results:
The Huffman and Shannon-Fano coding techniques have been successfully applied to
 the given source. The average codeword length, entropy, variance, redundancy, and
 efficiency have been computed.

