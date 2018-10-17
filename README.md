# FindCircle
Find a circle in the picture with Python 

#다음의 open CV 함수 사용
HoughCircles(image, method, dp, minDist[, circles[, param1[, param2[, minRadius[, maxRadius]]]]]) → circles
Parameters:	
image – 8-bit, single-channel, grayscale input image.
circles – Output vector of found circles. Each vector is encoded as a 3-element floating-point vector  (x, y, radius) .
circle_storage – In C function this is a memory storage that will contain the output sequence of found circles.
method – Detection method to use. Currently, the only implemented method is CV_HOUGH_GRADIENT , which is basically 21HT , described in [Yuen90].
dp – Inverse ratio of the accumulator resolution to the image resolution. For example, if dp=1 , the accumulator has the same resolution as the input image. If dp=2 , the accumulator has half as big width and height.
minDist – Minimum distance between the centers of the detected circles. If the parameter is too small, multiple neighbor circles may be falsely detected in addition to a true one. If it is too large, some circles may be missed.
param1 – First method-specific parameter. In case of CV_HOUGH_GRADIENT , it is the higher threshold of the two passed to the Canny() edge detector (the lower one is twice smaller).
param2 – Second method-specific parameter. In case of CV_HOUGH_GRADIENT , it is the accumulator threshold for the circle centers at the detection stage. The smaller it is, the more false circles may be detected. Circles, corresponding to the larger accumulator values, will be returned first.
minRadius – Minimum circle radius.
maxRadius – Maximum circle radius.

image – 흑백 처리된 사진만 사용가능
circles – Output vector of found circles. Each vector is encoded as a 3-element floating-point vector  (x, y, radius) .
circle_storage – In C function this is a memory storage that will contain the output sequence of found circles.
method – CV_HOUGH_GRADIENT 메소드만 사용가능
dp – 숫자가 높아질수록 낮은 해상도에서 처리, 1이면 원본 해상도, 2이면 절반 해상도 
minDist – 찾아낸 원의 중점 사이의 최대 거리, 즉 크면 클수록 원이 적게 잡힘
param1 – 크면 클수록 원이 적개 잡힘, 원 중심 잡는 thresh hold 값 상승
param2 – 크면 클수록 원이 적게 잡힘
minRadius – Minimum circle radius.
maxRadius – Maximum circle radius.
