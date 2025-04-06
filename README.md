# CIFAR-10-Machine-Learning-Model-Project

**Summary:**


This investigation consists of applying various classification methods to the CIFAR-10 dataset and analyzing the results
of each method. The classification methods we investigated were k-nearest neighbors (KNN), logistic regression, feedforward
neural networks, and random forest. We found that KNN gave an accuracy of 30.01%, logistic regression gave an accuracy of
38.51%, random forest gave an accuracy of 44.44%, and feedforward neural network gave an accuracy of 53.58%. We
concluded that the feedforward neural network is the best classifier to use for CIFAR-10 from the four classifiers we tested.


**Insights:**


1. KNN seems to have the best accuracy when classifying planes and ships. This could be due to the fact that planes are
found in the sky and ships are found in the sea, which means they have distinct background noise KNN can use as a
discriminator. The animal classes are often misclassified, likely due to the fact that animals such as dogs, cats, horses, and deer can have similar shades of fur while frogs and birds either have colors found in fur or vibrant colors found in backgrounds.


2. The logistic classifier struggled to accurately predict labels for classes 2, 3, and 4. This indicates a difficulty in
distinguishing between bird, cat, and deer images. This could be happening because as logistic regression is only able to assume linearity for features, these labels being animals with similar color could have similarity which make it difficult to predict. The precision (38.26%) and recall (38.51%) scores suggest that the model struggled to identify positive instances for these classes.


3. Logistic regression is efficient and interpretable, but it may not capture complex relationships between features.
We expected our random forest classifier to give us a higher accuracy score since it is a more sophisticated model.
However upon reflection, random forests wouldn't be good for perceptual data such as images because they don't do feature
extraction. We also could have improved the classifier's accuracy if we used a larger number of trees (n_estimators) when
training, but increasing the number of trees would lead to an increase in computational training, which isn't optimal. It is likely our results wouldn't differ by a large margin if we increased the number of trees in the forest.

4. According to the confusion matrix the feedforward neural network shows a bias against classifying pictures as deer and
a bias towards classifying pictures as birds. The error rate for both validation and training error reached their lowest point around 9 epochs. Additionally, The classifier could have been more successful if the parameters of the feedforward neural network were tuned according to a logical basis, instead of successively testing then implementing batches of parameters because the current approach failed to consider numerous hyperparameter combinations that may have been more effective.

5. Overall, the feedforward neural network was most effective in terms of accuracy in comparison with the other 3
classifiers. Further research should be done with other evaluation metrics outside of accuracy score, such as training speed and learning curves to further differentiate the differences between using the discussed classifiers on CIFAR-10.
