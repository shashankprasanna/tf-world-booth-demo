# tf-world-booth-demo

Download CIFAR-10 dataset and convert to tfrecord:

```
source activate tensorflow_p36
generate_cifar10_tfrecords.py --data-dir data
aws s3 mb s3://tf-booth-bucket
aws s3 sync data/ s3://tf-booth-bucket/cifar10-dataset/
