Model's average accuracy in this state is ≈0.9839 and the average loss is ≈0.0574.
I've started with rewriting the code from the lecture (1 conv layer, 1 hidden dense layer and 1 output dense layer), but it didn't work well, accuracy was about 0.05.
Then I've tried adding more dense layers but it gave no real result.
I thought that there might be some problem in the data input and that was it - input data wasn't normalized so model was getting numbers from 0 to 255 instead of 0 to 1.
I've added tf.keras.layers.Rescaling(1.0 / 255) and model's accuracy immediately jumped to values around 0.8.
Then I've found some examples of other models on the Internet and lots of them had more than one convolution layer.
So two more convolution layers were added, accuracy increased pretty well (to ≈0.98) and that was the final change of the model.
I've tried adding more than three convolution layers, increasing the filter amount in convolution layers, adding more dense layers, but it gave no visible results.
