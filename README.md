# UrbanSound8kClassifier

## Library To Use

We can use librosa library which can be installed using 
> pip install librosa

It uses ffmpeg as backend to convert and read some of the audio files. So to install ffmpeg, you can use 
> apt-get install ffmpeg

Librosa library can read audio files and convert them to there amplitude values for each sample of audio. Let us say there is an audio file of 4s and sampling rate of audio file is 22050 Hz. This means that audio file is made using amplitude samples such that 22050 samples of amplitudes are recorded in each second. Hence a 4s audio file with sampling rate 22050 can be expressed as an array of 4\*22050=88200 size 


## How to Load Audio Files and Extract Features

Using load method of librosa library, we can read audio files. It takes file path as input and returns an array having amplitude samples along with sampling rate of file.

Librosa library has many methods already build to extract features mentioned in resources which then returns another array of features.
We can use various combinations of those features.

For eg, in first stage you can extract only mfcc features and then build up a model and check the accuracy. Then try the same with other features. In order to further improve accuracy, you can also try to use more than one type of features and check the results.

## Using CNN to classify sound

This is a very classical way of sound classification as it is observed that similar type of sounds have similar spectrogram (read resource 3 to understand more about spectrogram). A spectrogram is a visual representation of the spectrum of frequencies of sound or other signal as they vary with time. And thus we can train a CNN network which takes these spectrogram images as input and using it tries to generalize patterns and hence classify them.
