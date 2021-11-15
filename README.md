# Eczema detection using transform domain analysis

We aim to create a system to detect eczema in human skin. Diagnosis of skin diseases is complex and carries a financial cost, while mobile phones have penetrated the most rural of places. We propose to use transform domain analysis to achieve our goal.


For our dataset, a 25X25 cross-section of each of the images is taken focused on the area of interest and converted into grayscale.
We start by finding the 2D wavelet transform for each image and take the LL sub-band discarding the remaining coefficients. We then calculate the GLCM to extract our features. After we create the GLCMs, several features can be derived from them using predefined formulae.
The features taken are: energy, contrast, dissimilarity, homogeneity, correlation, angular second moment and entropy. 
These features are then plotted in order to see if the values correlate with severity and thus verify if these features can be an indicator of the ailment. Once this is verified we can proceed to create and train our CNN model.
The features extracted during analysis are then used to train our model.
This model is then compiled, trained and validated using our feature vector to get our final results.
On training our model on 30 images and then validating on a set of 12 images, the model successfully predicts with an accuracy of 83.33%.
