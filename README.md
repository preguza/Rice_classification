Rice, which is among the most widely produced grain products worldwide, has many genetic varieties. These varieties are separated from each other due to some of their features. These are usually features such as texture, shape, and color. With these features that distinguish rice varieties, it is possible to classify and evaluate the quality of seeds. In this study, Arborio, Basmati, Ipsala, Jasmine and Karacadag, which are five different varieties of rice often grown in Turkey, were used. A total of 75,000 grain images, 15,000 from each of these varieties, are included in the dataset.

I have tested 2 approaches:
- Dimensionality reduction with PCA - from 250x250 pixels to 20 components. Then I have applied clasification algorithms (Decision Trees, Logistic Regression, Gradient Boosting etc);
- Classical computer vision (1 vanilla convnet and Mobile net with transfer learning).

Results are as follows:
- XGBClassifier reached an accuracy of 0.978 based on 20 features created with PCA. Inference time was only 0.01 seconds for 12500 examples. Similar results achieved LGBMClassifier and SVM;
- Classical convolutional networks took more than 30 seconds for inference and achieved accuracies of 0.91;
- Other algorithms such as Logistic regression, Decision Tree, Random Forest showed less acurate results.

I suggest using XGBClassifier given the high accuracy and low computational need. It It is most suited for edge devices in industrial applications.

Means for further improvement:
- Training algorithms on more PCA components (compared to 20 in this notebook);
- Using ensembles;
- Hyperparameter tunning.
