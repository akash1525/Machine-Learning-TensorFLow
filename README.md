learn machine learning techs
============================
Ren Ye 2016-11-02

## CONTENTS ##
+ image recpgnition with TensorFlow
+ time series forecasting with R
+ text classification with TensorFlow

## image recognition with TensorFlow ##
prerequisite: *tensorflow*, *tensorflow for poets*, `circle`, `cruciform`, `triangle` directories in `tf_4_poets/robotx_shapes/`

```bash
# training
cd ~/Tensorflow_learn/tensorflow/
python tensorflow/examples/image_retraining/retrain.py \
--bottlenect_dir=../tf_4_poets/robotx_shapes/bottlenecks \
--model_dir=../tf_4_poets/robotx_shapes/inception \
--output_graph=../tf_4_poets/robotx_shapes/retrained_graph.pb \
--output_labels=../tf_4_poets/robotx_shapes/retrained_labels.txt \
--image_dir ../tf_4_poets/robotx_shapes/shape_photos
#
# testing
cd ~/Tensorflow_learn/tf_4_poets/
# test triangle
python robotx_shapes/label_image.py robotx_shapes/shape_photos/triangle/n13879816_14.JPEG
# test circle
python robotx_shapes/label_image.py robotx_shapes/shape_photos/triangle/n03032811_27724.JPEG
# test cruciform
python robotx_shapes/label_image.py robotx_shapes/shape_photos/triangle/n03032811_20080.JPEG
```
