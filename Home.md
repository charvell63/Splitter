**Spleeter** is the [Deezer](https://www.deezer.com/) source separation library with pretrained models written in [Python](https://www.python.org/) and uses [Tensorflow](tensorflow.org/) (only v1 is supported for now). It makes it easy to train source separation model (assuming you have a dataset of isolated sources), and provides already trained state of the art model for performing various flavour of separation.

The separation process can be performed both on *GPU* or *CPU*. It is very fast when run on *GPU*: for instance, the whole [musDB](https://sigsep.github.io/datasets/musdb.html) test set (about 3h27m of audio) is separated in less than 90s on a single *Nvidia GeForce GTX 1080* (audio loading and writing is done on a 32 core *Intel(R) Xeon(R) Gold 6134 CPU @ 3.20GHz*).

This documentation provides:

 * [Installation](/deezer/spleeter/wiki/1.-Installation) instructions
 * [Usage manual](/deezer/spleeter/wiki/2.-Getting-started) to get you started
 * A deeper view of the [Python API](/deezer/spleeter/wiki/4.-API-Reference) and the pretrained [Models](/deezer/spleeter/wiki/3.-Models) packaged with **Spleeter**