I used opencv to determine top eye edge parabola coefficients using opencv and numpy and compare it with coefs from other software i was given.
This work consists of aplying several methods in a row:
1) Sobel filter among y axis to get derivative field, which corresponds horizontal edges.
2) Median filter to remove small gradient changes especially in eyelashes.
3) Adaptive threshholding to remove noise.
4) Mathematical morphology to connect incoherent parts.
5) cv2.findContours to get potential points for parabola approximation.
6) Numpy polynomial fit to get parabola coeffs.
