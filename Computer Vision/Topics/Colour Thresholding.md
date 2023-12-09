### **Topics Mentioned**
- [Back Projection](../../Computer%20Vision/Topics/Back%20Projection.md)

### Code Example
```c++
cv::Mat hsvImage;
    cv::cvtColor(image, hsvImage, cv::COLOR_BGR2HSV);

    // Define the lower and upper bounds for the color you want to threshold
    cv::Scalar lowerBound(30, 50, 50); // Lower HSV values for the color (in this case, green)
    cv::Scalar upperBound(90, 255, 255); // Upper HSV values for the color (in this case, green)

    // Create a mask using inRange function to threshold the image based on the defined color range
    cv::Mat mask;
    cv::inRange(hsvImage, lowerBound, upperBound, mask);
```


### Explanation of Function
This is a primitive way of isolating colour. It is not as accurate as Back Projection but is very easy to implement. Ken hates this way.