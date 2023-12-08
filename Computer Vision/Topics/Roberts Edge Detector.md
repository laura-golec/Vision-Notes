---
title: Roberts Edge Detector
updated: 2023-12-08 17:36:10Z
created: 2023-12-08 16:45:46Z
latitude: 53.82059030
longitude: -7.76841400
altitude: 0.0000
---

## Excerpts from His Book
![4294000fc01c13c4cfcdbd4cd63fa38a.png](../../_resources/4294000fc01c13c4cfcdbd4cd63fa38a.png)
![8d70c2ca996d31c3b9d2f5616affba3d.png](../../_resources/8d70c2ca996d31c3b9d2f5616affba3d.png)
![85ee08e00f1ddf5af405aa53722f0166.png](../../_resources/85ee08e00f1ddf5af405aa53722f0166.png)

---

### **Relevant Topics**
- [First Derivative Edge Detection](../../Computer%20Vision/Topics/First%20Derivative%20Edge%20Detection.md)
- [Compass Edge Detectors](../../Computer%20Vision/Topics/Compass%20Edge%20Detectors.md)

### Explanation of Function
This partial derivative is ideal only in binary images. It works best when edges are only 1 pixel wide as it compares points on an adjacent basis. It detects edges perfectly on a binary image but is not very useful in gradient situations. 

It also calculates the edges as 1/2 a pixel out from the actual edges. 
