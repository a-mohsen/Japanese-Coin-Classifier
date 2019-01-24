## Japanese Coin Classifier

![enter image description here](https://lh3.googleusercontent.com/y0xSNmb5cHf2z4AZSTRBfyITMM20dgYeS7ZH7MoegMIrnOe79UkoIUMExfxa2SD33vHQPZYKt_Ne)

This is a YOLO3 classifier for Japanese coins.
The following dataset was used to train the classifier:

[https://drive.google.com/open?id=1-_JkQ7E8N0toHYVHFKTuzugOg_OQMfEO](https://drive.google.com/open?id=1-_JkQ7E8N0toHYVHFKTuzugOg_OQMfEO)

https://drive.google.com/open?id=1GUXLuv95ixrZYHcpM0JnWHUHoc_hk--k

https://drive.google.com/open?id=1n-4PwJUWzmUQuHnLwhnzQeVrYt_qrn_z

https://drive.google.com/open?id=1YjCo09Rh9pdtU44jR3eoG8GqmVchxhj_

https://drive.google.com/open?id=1SmHncEczhsGXXTBUUsaVFUPBVh-PWWF1

https://drive.google.com/open?id=1PMs6Q3Z08skZWCAmjBtd8-Sff9R_I6Z5

It contains 6 classes (1 - 5 - 10 - 50 - 100 - 500 Yen). Each class has 300 images.
The data is split into 90% training and 10% for testing.

The dataset had been built from Google Images using the [script from PyImageSearch](https://www.pyimagesearch.com/2017/12/04/how-to-create-a-deep-learning-dataset-using-google-images/)

It had been filtered manually, then [Augmentor library](https://github.com/mdbloice/Augmentor) was used to increase the of images for each class (by zooming, cropping, rotating, etc..)  

Finally, the data was labeled using [BBox-Label-Tool](https://github.com/puzzledqs/BBox-Label-Tool)

The training procedures was implemented on Google Compute Engine instance with Tesla K80 (to use CUDA for training).

The latest weight file (10000 iterations) can be found on this link:

https://drive.google.com/open?id=1nLIT9OwG00tB40QU52_mb-b1dLJ6DujM

It has average loss of 0.2, although it's still needs more training, as it can barely draw the bounding rectangles (in the previous weight file, it couldn't even identify or draw bounding boxes).
Please feel free to fork the repository and continue the training.


  

