# level-4-dissertation

#Notes

http://people.csail.mit.edu/matei/papers/2012/nsdi_spark.pdf
http://people.csail.mit.edu/matei/papers/2010/hotcloud_spark.pdf
http://www.jmlr.org/papers/volume17/15-237/15-237.pdf

RDD, DAC, Legacy, Lineage, Narrow - Wide dependency, Hadoop

DenseVector - contains all values, SparseVector - removes zeroes and maintains an array of indecies for the non zero values

Kmeans run() - takes RDD of dense vectors
In input file each line is a dot in 3D space
runAlgorithm() - takes RDD of VectorWithNorm