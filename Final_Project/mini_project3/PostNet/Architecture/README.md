In Postnet we have 5 convolution layers which is comprised of 512 filters with shape 5 × 1 this is a large neural networks and can potentially overfit the data and result in poor performance so we used **drop out** at the end of each layer, Dropout is a regularization method that approximates training a large number of neural networks with different architectures in parallel

The changes are made in in the file https://github.com/coqui-ai/TTS/blob/c410bc58ef3bd07b72ab05d29bbdc2a6df47afea/TTS/tts/layers/tacotron/tacotron2.py as shown in tactron2.py
