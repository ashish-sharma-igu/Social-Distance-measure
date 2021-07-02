Object detection:

We will be using YOLOv3, trained on COCO dataset for object detection.
In general, single-stage detectors like YOLO tend to be less accurate than two-stage detectors (R-CNN) but are significantly faster.
YOLO treats object detection as a regression problem, taking a given input image and simultaneously learning bounding box coordinates and corresponding class label probabilities.
It is used to return the person prediction probability, bounding box coordinates for the detection, and the centroid of the person.
Distance calculation:

NMS (Non-maxima suppression) is also used to reduce overlapping bounding boxes to only a single bounding box, thus representing the true detection of the object. Having overlapping boxes is not exactly practical and ideal, especially if we need to count the number of objects in an image.
Euclidean distance is then computed between all pairs of the returned centroids. Simply, a centroid is the center of a bounding box.
