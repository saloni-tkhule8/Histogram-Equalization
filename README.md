# Histogram-Equalization

Histogram Equalization is a technique in image processing used to enhance contrast in an image. It works by redistributing the intensity values so that they span the entire available range more evenly. This method is particularly useful for improving the visibility of details in images with poor contrast.

**How Histogram Equalization Works:**
        
    1.Calculate Histogram: Count the number of pixels for each intensity level in the image.
    2.Compute CDF (Cumulative Distribution Function): The CDF is derived from the histogram and helps in mapping intensity values.
    3.Normalize the CDF: Scale the CDF so that the minimum value is mapped to 0 and the maximum to 255 (for an 8-bit image).
    4.Map New Intensity Values: Replace each pixel’s intensity with its corresponding new value from the equalized histogram.

Mathematical Representation:
Let 
𝑓
(
𝑥
,
𝑦
)
f(x,y) be the original image with intensity values in the range 
[
0
,
𝐿
−
1
]
[0,L−1].

Probability Distribution Function (PDF):

𝑃
𝑟
(
𝑟
𝑘
)
=
𝑛
𝑘
𝑀
𝑁
P 
r
​
 (r 
k
​
 )= 
MN
n 
k
​
 
​
 
where:

𝑟
𝑘
r 
k
​
  is the intensity level
𝑛
𝑘
n 
k
​
  is the number of pixels with intensity 
𝑟
𝑘
r 
k
​
 
𝑀
×
𝑁
M×N is the total number of pixels in the image
Cumulative Distribution Function (CDF):

𝐶
𝐷
𝐹
(
𝑟
𝑘
)
=
∑
𝑗
=
0
𝑘
𝑃
𝑟
(
𝑟
𝑗
)
CDF(r 
k
​
 )= 
j=0
∑
k
​
 P 
r
​
 (r 
j
​
 )
Transformation Function:

𝑠
𝑘
=
(
𝐿
−
1
)
×
𝐶
𝐷
𝐹
(
𝑟
𝑘
)
s 
k
​
 =(L−1)×CDF(r 
k
​
 )
where 
𝑠
𝑘
s 
k
​
  is the new intensity level.
