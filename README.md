# VAE_MNIST
Understand how VAE works, capabilities and use in Industry.
When we work on anomaly detection projects in the industrial world, on equipment failure prediction for example, we generally have “unbalanced” data, that is to say that the data The vast majority of data reflect a satisfactory condition of the equipment and very few that show deterioration.
And this situation is not favorable to model training where balance is sought and must be achieved.

Fortunately, in AI, we never run out of ideas…

Auto encoders can help solve this problem, and more particularly “variational auto encoders” (or VAE, it’s simpler).
The VAE is an unsupervised model, which extracts the most characteristic information from the input data and then seeks to reconstruct the input data from the essential characteristics of this data.

The model actually learns a distribution of the input data and this is precisely what interests us.
Indeed, if a data flow from a sensor shows a distribution which deviates from that learned by the model (there is a notion of threshold to understand, characteristic of the operation of the equipment), then there is operation abnormal and production of an alert.
This is why VAEs are relevant in this type of context!

Another interesting characteristic is that VAEs are generative models since they seek to reconstruct the input data from a few essential characteristics.
From an input image, the model generates similar images which gradually, as training progresses, “deviate” from the input image to “marry” the contours of another image whose distribution is close.
![espace latent](https://github.com/DSAGRO3F/VAE_MNIST/blob/main/rep_espace_latent_tsne)
