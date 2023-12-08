---
title: Compass Edge Detectors
updated: 2023-12-08 17:47:15Z
created: 2023-12-08 16:46:04Z
latitude: 53.82059030
longitude: -7.76841400
altitude: 0.0000
---

## Excerpts from His Book
![ee063fcc3db34dfa1dee472491e7e978.png](../../_resources/ee063fcc3db34dfa1dee472491e7e978.png)
![18c79c151651641b2d39f068a54be115.png](../../_resources/18c79c151651641b2d39f068a54be115.png)
![587e5c52190e0647d858c046af7d7c43.png](../../_resources/587e5c52190e0647d858c046af7d7c43.png)

---

### **Relevant Topics**
- [First Derivative Edge Detection](../../Computer%20Vision/Topics/First%20Derivative%20Edge%20Detection.md)
- [Roberts Edge Detector](../../Computer%20Vision/Topics/Roberts%20Edge%20Detector.md)

### Code Example
```c++
Mat horizontal_derivative, vertical_derivative;
Sobel( gray_image, horizontal_derivative, CV_32F ,1,0 );
Sobel( gray_image, vertical_derivative, CV_32F,0,1 );
```

### Explanation of Function
This function takes the changes in pixels on a vertical and horizontal axis (although more axis are possible, hence the compass name). These changes are represented in various shades of grey. They are then thresholded so that only changes of a certain significance are considered. This allows us to work on greyscale images, unlike Roberts Edge Detector. It's not as clean, but provides a good basis for further refinement. 

The only difference between the Sobel and Prewitt variants is the weighting of the smoothing filter. Due to this, we can essentially ignore this difference and treat them as the same.