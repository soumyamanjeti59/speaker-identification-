# speaker-identification
CONTEXT

Speaker Recognition has always been a cool part to work on in AI.

CONTENT

This dataset contains speeches of five prominent leaders namely; Benjamin Netanyahu, Jens Stoltenberg, Julia Gillard, Margaret
Tacher and Nelson Mandela which also represents the folder names. Each audio in the folder is a one-second 16000 sample rate PCM encoded.
Originally, the speech for each speaker was a one lengthy audio, I chunked them into one-second each for easier workability. If you combine the chunked audios from 0.wav to 1500.wav, it forms a complete speech of the respective speaker.

A folder called background_noise contains audios that are not speeches but can be found inside and around the speaker environment e.g audience laughing or clapping. It can be mixed with the speech while training.

INSPIRATION

It is somewhat challenging to build small speech recognition models which are very accurate. My goal for this dataset is to develop models that are small enough to be deployed on an mobile device with less compute but at the same time be more accurate. You can
refer to this project to see what have done.

IMPORTED FILES

tensor flow

os

numpy

shutil

keras

After importing necessary libraries i arranged the audio and noise 
then get the list of all noices then after few lines of code,i splitted noice into chunks of 16000 steps each.
Data set is generated and noises added to the dataset.
Shuffle to generate random data.
Split into training and validation.
Create datasets,one for training and another for validation

UNDER FEATURE EXTRACTION

Add noise to the training set.
Transform audio wave to the frequency domain using `audio_to_fft`

Modelling is done.

Training is done and epochs are created.

ACCURACY

In the beginning the accuracy is low, as more epochs are executed the accuracy increases and loss significantly decreases.

PREDICTION

Based on real time we are giving the speaker to be predicted and the model predicts the speaker based on training data.
