---
**Date: 21-09-2024  
**Experiment: 1  
---

---
**Name**: Nikhil  
**Reg. No.**: 24900366  
---

# Aim:
To find the mean and variance of the arrival of objects from the feeder using probability distribution.

---

# Software Required:
- Python  
- Visual Components Tool  

---

# Theory:
The expectation or the mean of a discrete random variable is a weighted average of all possible values of the random variable. The weights are the probabilities associated with the corresponding values. 

It is calculated as:  

![Expectation Formula](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables. It indicates the distance of a random variable from its mean.  

It is calculated as:  

![Variance Formula](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)

---

# Procedure:
1. Construct a frequency distribution for the data.  
2. Find the probability distribution from the frequency distribution.  
3. Calculate the mean using:  

   ![Mean Formula](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Calculate \( E[X^2] \):  

   ![E[X^2] Formula](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5. Calculate the variance using:  

   ![Variance Formula](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)

---

# Experiment:
Input the data values and calculate their mean, variance, and standard deviation using the program below.

---

# Program:

```
import numpy as np

L = [int(i) for i in input().split()]
N = len(L)
M = max(L)

x = []
f = []

for i in range(M + 1):
    c = 0
    for j in range(N):
        if L[j] == i:
            c += 1
    f.append(c)
    x.append(i)

sf = np.sum(f)
p = [f[i] / sf for i in range(M + 1)]

mean = np.inner(x, p)
EX2 = np.inner(np.square(x), p)
var = EX2 - mean**2
SD = np.sqrt(var)

print("The Mean arrival rate is %.3f " % mean)
print("The Variance of arrival from feeder is %.3f " % var)
print("The Standard deviation of arrival from feeder is %.3F " % SD)
```
# Output : 
![image](https://github.com/user-attachments/assets/32a799ff-5a3e-4680-ba8d-e35a2b8d531a)

# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.
