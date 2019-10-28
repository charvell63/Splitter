**Spleeter** is the [Deezer](https://www.deezer.com/) source separation library with pretrained models.
It is written in [Python](https://www.python.org/) and uses [Tensorflow](tensorflow.org/) (only v1 is supported for now):

* It provides already trained state of the art model for performing separation 
* It makes it easy to train source separation model with [Tensorflow](tensorflow.org/) (provided you have a dataset of isolated sources).

This documentation provides:
 * [Installation](../1.-Installation) instructions
 * [Usage manual](../2.-Getting-started) to get you started
 * A deeper view of the [Python API](../4.-API-Reference) and the pretrained [Models](../3.-Models) packaged with **Spleeter**

The separation process can be performed both on *GPU* or *CPU*. It is very fast when run on *GPU*: for instance, the whole [musDB](https://sigsep.github.io/datasets/musdb.html) test set (about 3h27m of audio) is separated in less than 90s on a single *Nvidia GeForce GTX 1080* (audio loading and writing is done on a 32 core *Intel(R) Xeon(R) Gold 6134 CPU @ 3.20GHz*).
