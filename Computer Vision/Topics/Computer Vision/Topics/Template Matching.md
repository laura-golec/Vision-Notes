## Excerpts from His Book
![b30c0e6231065395ca3ac79eea4b8b26.png](../../_resources/b30c0e6231065395ca3ac79eea4b8b26.png)
![782f0e3d046d19866ce3d9a3a39e02fc.png](../../_resources/782f0e3d046d19866ce3d9a3a39e02fc.png)
![1187b7f94e9376e3dbd28e9e2222b494.png](../../_resources/1187b7f94e9376e3dbd28e9e2222b494.png)
![d96416e966438643f317beb1f6e6b7e2.png](../../_resources/d96416e966438643f317beb1f6e6b7e2.png)
![5e4b6974c9638bf997d318dcd337488a.png](../../_resources/5e4b6974c9638bf997d318dcd337488a.png)
![d617492f518f4a19047a9b80dcdcd400.png](../../_resources/d617492f518f4a19047a9b80dcdcd400.png)
![657a169ba61c56ac832e925d044fe694.png](../../_resources/657a169ba61c56ac832e925d044fe694.png)

### **Topics Mentioned**

### Code Example
```c++
Mat matching_space;
matching_space.create(
	search_image.cols–template_image.cols+1,
	search_image.rows–template_image.rows+1, CV_32FC1 );
matchTemplate( search_image, template_image,
				matching_space, CV_TM_CCORR_NORMED );
```
There is just a built in function to do template matching.

### Explanation of Function
This function is used when searching for a known target within an image. Reference images for what the target looks like are provided. The pixels of the target image are then compared to the pixels in an area of the image we are searching. After this, each pixel is converted to the sum of the squared differences. Therefore, the pixel with the lowest value is considered the most likely centre of the match.

There are a few issues with this approach. One of them being that it is highly sensitive to any geometrical deformations (such as a perspective warp). It is also highly susceptible to generating multiple positive matches in a small area. To avoid this, the area searched should be larger. 

The amin issue however is how costly this matching is. It requires a lot of computational power, especially on higher resolution images as it goes pixel by pixel. One of the proposed solution is to first scale the image down and try to find a likely match location within this lower resolution image. Then to search only in the area of the likely match in the higher resolution image. The issue is that this might cause us to lose out on some matches. 

### Sample Questions
2019 Exam Paper Question 3.b.
![c46e95fb0b6c610ca421cdaaaa87e6a7.png](../../_resources/c46e95fb0b6c610ca421cdaaaa87e6a7.png)