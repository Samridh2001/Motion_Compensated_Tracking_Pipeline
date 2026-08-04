# Motion-Compensated-Tracking-Pipeline

Model Integration: Utilizes Roboflow's DEtection Transformer (rfdetr-large) for initial object detection with a minimum confidence threshold of 0.2.

Motion Stabilization: Implements a MotionEstimator to calculate coordinate transformations, compensating for camera movement during tracking.

Target Filtering: Applies Non-Maximum Suppression with a 0.3 threshold, filtering detections to specifically isolate Persons, Cars, and Birds.

Object Tracking: Leverages the ByteTrackTracker to maintain consistent IDs across consecutive frames.

Advanced Annotation: Uses the supervision package to draw bounding boxes, custom ID labels, and motion-aware trajectory traces on the video frames.

Video Export: Compresses the processed output using ffmpeg to ensure the final tracked video is web-ready and natively displayable.
