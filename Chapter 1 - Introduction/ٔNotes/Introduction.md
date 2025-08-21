

#Fact  Every second, the microphone will collect roughly 44,000 samples.


## **Notes**
Once the parameters are fixed, we call the program a **model**. The set of all distinct programs (input–output mappings) that we can produce just by manipulating the parameters is called a **family of models**. And the [[Meta Programming]] that uses our dataset to choose the parameters is called a **learning algorithm**.


Features (sometimes called covariates or inputs)


We call the (constant) length of the input vectors the **dimensionality** of the data.


One major advantage of deep learning over traditional methods is the comparative grace with which modern models can handle varying-length data.


Deep learning is differentiated from classical approaches. These models consist of many successive **transformations of the data** that are chained together top to bottom, thus the name deep learning.


we need to have formal measures of how good (or bad) our models are. we call these **objective functions**. By convention, we usually define objective functions so that lower is better. ==Because we choose lower to be better, these functions are sometimes called loss functions.==


During optimization, we think of the loss as a function of the model’s parameters, and treat the training dataset as a constant.


Popular optimization algorithms for deep learning are based on an approach called [[Gradient descent]] In brief, at each step, this method checks to see, for each parameter, how that training set loss would change if you perturbed that parameter by just a small amount. It would then update the parameter in the direction that lowers the loss.
(Check [[How does gradient descent works]])



In probabilistic terms, we typically are interested in estimating the conditional probability of a label given input features. 
#### My Mind :
y|x in which x is features and y is label .


We feed the training dataset into a supervised learning algorithm, a function that takes as input a dataset and outputs another function: **the learned model.** Finally, we can feed previously unseen inputs to the learned model, using its outputs as predictions of the corresponding label.


**Squared error loss function**. As we will see later, this loss corresponds to the assumption that our data were corrupted by [[Gaussian noise]].


Common loss function for classification problems is called **cross-entropy**.([[Cross Entropy]])



There are some variants of classification addressing **hierarchically structured classes**. In such cases ==not all errors are equal—if we must err==, we might prefer to misclassify to a related class rather than a distant class. Usually, this is referred to as hierarchical classification. For inspiration, you might think of Linnaeus 20 , who organized fauna in a hierarchy.  In the case of animal classification, it might not be so bad to mistake a poodle for a schnauzer, but our model would pay a huge penalty if it confused a poodle with a dinosaur.