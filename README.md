# M-ADDA: Metric-based Adversarial Discriminative Domain 

To obtain the test results, run the following command,

```
python main.py -e usps2mnist mnist2usps uspsBig2mnistBig mnistBig2uspsBig -m test_model
```

The output should be,

```
mnist2usps          0.955676
mnistBig2uspsBig    0.980541
usps2mnist          0.951500
uspsBig2mnistBig    0.983100
```
which represent the accuracies obtained on the target test set.

- mnistBig, and uspsBig use the full training set.
- mnist, and usps use 2000 images from MNIST and 1800 images from USPS for training, respectively.

To train the source and target models run the command,

```
python main.py -e usps2mnist mnist2usps uspsBig2mnistBig mnistBig2uspsBig -m train -rt 1 -rs 1
```
Source (MNIST)            |  Target (USPS)
:-------------------------:|:-------------------------:
![](figures/src_mnistBig2uspsBig.png)  |  ![](figures/tgt_mnistBig2uspsBig.png)
