# level-4-dissertation

#Notes

http://people.csail.mit.edu/matei/papers/2012/nsdi_spark.pdf - RDD description

http://people.csail.mit.edu/matei/papers/2010/hotcloud_spark.pdf - Spark basics

http://www.jmlr.org/papers/volume17/15-237/15-237.pdf - Spark MLlib basics

https://ocw.mit.edu/courses/sloan-school-of-management/15-097-prediction-machine-learning-and-statistics-spring-2012/projects/MIT15_097S12_proj1.pdf - Lloyd's online k-means

https://www.eecs.tufts.edu/~dsculley/papers/fastkmeans.pdf - mini-batch k-means


RDD, DAC, Legacy, Lineage, Narrow - Wide dependency, Hadoop

DenseVector - contains all values, SparseVector - removes zeroes and maintains an array of indecies for the non zero values

Kmeans run() - takes RDD of dense vectors

In input file each line is a dot in 3D space

runAlgorithm() - takes RDD of VectorWithNorm

Clustering objectives:
minimize the mean squared distance from all points to  their  respective  cluster  centers

#Porject use

Rebuilding project: build/mvn -DskipTests clean package

Launch shell: ./bin/spark-shell

Simple shell command: sc.parallelize(1 to 1000).count()