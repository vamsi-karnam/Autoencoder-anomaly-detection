# Anomaly Detection using Autoencoder architecture
Building an Autoencoder to detect anomalies in data

# Datasets
1. Warblr and Freefield datasets: These datasets contain audio files that are labeled as either containing bird calls or not. They are used for training the model.
2. Chernobyl dataset: This is an unlabelled dataset that contains audio files for which the presence of bird calls is unknown. It is used for testing the model.

# Methodology
The project uses a Variational Autoencoder (VAE), a type of deep learning model, to classify the audio files. The VAE is trained on the Warblr and Freefield datasets to learn how to reconstruct audio files that contain bird calls. Once trained, the VAE can take an audio file as input and attempt to reconstruct it. The difference between the original audio file and the reconstructed version is known as the reconstruction loss.
- If an audio file contains a bird call, the VAE should be able to reconstruct it well, resulting in a low reconstruction loss. Conversely, if an audio file does not contain a bird call, the VAE will likely struggle to reconstruct it accurately, leading to a high reconstruction loss.
- By comparing the reconstruction loss of an audio file to a threshold value, we can classify it as containing a bird call (if the loss is below the threshold) or not (if the loss is above the threshold).

## References

Data source:

[1] [Bird Audio Detection Challenge](https://machine-listening.eecs.qmul.ac.uk/bird-audio-detection-challenge/)
> D. Stowell, M. Wood, Y. Stylianou, and H. Glotin, “Bird detection in audio: a survey and a challenge,” arXiv preprint arXiv:1608.03417, 2016.

[2] [Deep Learning for Anomaly Detection: A Survey](https://arxiv.org/abs/1901.03407)
> Chalapathy, R., Chawla, S., “Deep Learning for Anomaly Detection: A Survey,” arXiv preprint arXiv:1901.03407, 2019.

[3] [VAE's vs GAN's for Anomaly Detection](https://www.linkedin.com/advice/3/what-advantages-disadvantages-gan-vae-anomaly-detection#:~:text=Disadvantages%20of%20GAN,-GANs%20have%20some&text=GANs%20are%20not%20genuinely%20built,broad%20range%20of%20data%20representations)
> “What are the advantages and disadvantages of GAN over VAE in anomaly detection?” LinkedIn.
