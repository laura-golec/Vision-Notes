## Excerpts from His Book
![c56bd1783788c785d0ab699895d22621.png](../../_resources/c56bd1783788c785d0ab699895d22621.png)
![0a619195799c9ff425cc1117f1954058.png](../../_resources/0a619195799c9ff425cc1117f1954058.png)

---

### **Topics Mentioned**
- [Colour Thresholding](../../Computer%20Vision/Topics/Colour%20Thresholding.md)

### Code Example
```c++
calcHist ( &hls_samples_image, 1, channel_numbers, Mat(),
	histogram,image.channels(),number_bins,channel_ranges);
normalize ( histogram, histogram, 1.0);
Mat probabilities = histogram.BackProject ( hls_image );
```


### Explanation of Function
Essentially you create a histogram of the probability of a colour being your target. You then project that information onto an image and set a certain threshold above which a pixel is marked as your target colour. This is far better than regular colour thresholding, and Ken much prefers it.