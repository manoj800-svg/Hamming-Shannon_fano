# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
- Python with NumPy and SciPy libraries.
- Google Colab
# Program:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}") 
```
# Calculation:

![WhatsApp Image 2025-09-11 at 19 54 13_d79a5c11](https://github.com/user-attachments/assets/da0b1bfc-49a1-46b3-a4d5-67b1e088d880)
![WhatsApp Image 2025-09-11 at 19 54 13_a36ccc8f](https://github.com/user-attachments/assets/dfedf6cc-3ef1-4bc1-aa2e-d9ec123d1645)


# Output

<img width="548" height="561" alt="image" src="https://github.com/user-attachments/assets/0bd90181-20d7-41e4-b345-70b67dabf2a3" />

# Results:

The Huffman and Shannon-Fano coding techniques have been successfully applied to the given source. The average codeword length, entropy, variance, redundancy, and efficiency have been computed.
