# camera_caliberation_and_image_undistortion
The code uploaded consists of a pipeline that can be used for image undistortion to remove barrel and pin cushion distortion. The pipline consists of the following steps:
1. Out of 50 images of a chess pattern those images are first filtered out that can have their chessboard corners detected and these images are stored for further processing.
2. For the images that can get their chessboard corners detected they are undistorted then by using their chessboard corners and the function cv2.getOptimalNewCameraMatrix for getting the optimal camera matrix and then using
   the cv2.undistort to undistort the image.
3. For visualization purposes those undistorted images that can get their chessboard corners detected are further filtered and saved. Later the original image is taken, its undistorted version is used to calculate corners for that image.
   Later then the undistorted corners along with the original corners are plotted.
Consider the following example image:


<img src="https://github.com/user-attachments/assets/cde475b6-1913-4954-a233-9458f31c5967" width="500" height="300">


Also consider the following image that has both the undistorted and original corners plotted on it.


<img src="https://github.com/user-attachments/assets/28d4ae65-4c36-4397-850e-1fee1fd53fdb" width="500" height="300">
