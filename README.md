# HandWritten-Line-Recognition-System-

Description

Use Convolution neural network to recognize the handwritten line text image without pre-segmentation into words or characters.

How it works?

1. First Use Convolutional Recurrent Neural Network to extract the important features from the handwritten line text Image.
2. The output before CNN FC layer (512x100x8) is passed to the BLSTM which is for sequence dependency and time-sequence operations.
3. Then CTC LOSS Alex Graves is used to train the RNN which eliminate the Alignment problem in Handwritten, since handwritten have different alignment of every writers. 4.
4. We just gave the what is written in the image (Ground Truth Text) and BLSTM output, then it calculates loss simply as -log("gtText"); aim to minimize negative maximum likelihood path.
5. Finally CTC finds out the possible paths from the given labels.
6. Finally CTC Decode is used to decode the output during Prediction.

Requirements 

Tensorflow. Flask 1.1.1, Numpy, OpenCV.

Dataset - IAM Handwritten Dataset



