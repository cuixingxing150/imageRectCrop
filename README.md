# Image Rotated Rectangle Crop

[![View on File Exchange](https://www.mathworks.com/matlabcentral/images/matlab-file-exchange.svg)](https://ww2.mathworks.cn/matlabcentral/fileexchange/107539-image-crop)

[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=cuixing158/imageRectCrop&file=main.mlx)

An enhanced version of matlab's built-in function [imcrop](https://ww2.mathworks.cn/help/images/ref/imcrop.html), supporting rotated rectangle crop.

## Example

```matlab
srcImg = imread('peppers.png');
cropRect = [260,200,80,200,pi/4];% [centerX,centerY,width,height,yaw]

% crop rotate rectangle image
cropedImg = imgCrop(srcImg,cropRect);

% show result
rect = [cropRect(1:4),cropRect(5)*180/pi];
verticles = getVertices(rect);
p = polyshape(verticles(:,1),verticles(:,2));
figure;imshow(srcImg);hold on; plot(p);title('origin image');
```

![1](1.jpg)

```matlab
figure;imshow(cropedImg);title('cropped image')
```

![2](2.jpg)
