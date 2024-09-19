Instructions About Experiment 2

Data Partition:

Download the CIFAR-10 data and separate them into training and test sets.
CIFAR-10 training set is partitioned into two parts: D with 40,000, H with 20,000 examples.
Partitioned D into 10 clients with 1-class non-IID data for each client.
H is used to create 2 random subsets with β =10% and β= 20%
H is used to create 10 random subsets with α ranging from 0% to 100% (0% 10%, 20%,......)
Merger each subset of α data with each client data of 10 client
Now we have 10 clients with 1-class non-IID data + data from random subset

FL construction:
Construct a CNN and initially trained it with β =10% data
Update FL model based on separated data before using FedAvg algorithm (60.0%)

Estimate Accuracy:
Get the test accuracy of the global model using test data
Change the α value to (0%, 10%, 20%,.....) and train the model and get test accuracy
Repeat the above experiments when β =20%

Plot the Graph:
Plot the two accuracy graph when β=10%, 20% and α=0%, 10%, 20%,.....,100.0% 
