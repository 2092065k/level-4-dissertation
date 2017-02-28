# level-4-dissertation

#Notes

http://people.csail.mit.edu/matei/papers/2012/nsdi_spark.pdf - RDD description

http://people.csail.mit.edu/matei/papers/2010/hotcloud_spark.pdf - Spark basics

http://www.jmlr.org/papers/volume17/15-237/15-237.pdf - Spark MLlib basics

https://ocw.mit.edu/courses/sloan-school-of-management/15-097-prediction-machine-learning-and-statistics-spring-2012/projects/MIT15_097S12_proj1.pdf - Lloyd's online k-means

https://www.eecs.tufts.edu/~dsculley/papers/fastkmeans.pdf - Mini-batch k-means

http://cs.du.edu/~mitchell/mario_books/Introduction_to_Machine_Learning_-_2e_-_Ethem_Alpaydin.pdf - Machine learning

http://ac.els-cdn.com/0377042787901257/1-s2.0-0377042787901257-main.pdf?_tid=4b586634-c0aa-11e6-a748-00000aacb35e&acdnat=1481575012_a2f4e7407c483e9bb6f564a0c7f9bfaa - Silhouette


RDD, DAC, Legacy, Lineage, Narrow - Wide dependency, Hadoop

DenseVector - contains all values, SparseVector - removes zeroes and maintains an array of indecies for the non zero values

Kmeans run() - takes RDD of dense vectors

In input file each line is a dot in 3D space

runAlgorithm() - takes RDD of VectorWithNorm

Clustering objectives:
minimize the mean squared distance from all points to  their  respective  cluster  centers

#Porject use

Rebuilding project: build/mvn -DskipTests clean package

Create a local distribution: ./dev/make-distribution.sh --name custom-spark --tgz -DskipTests

Create a disribution on the cluster: ./dev/make-distribution.sh --name custom-spark --tgz -Phadoop-2.6 -Phive -Phive-thriftserver -Pyarn -DskipTests

Launch shell: ./bin/spark-shell

Simple shell command: sc.parallelize(1 to 1000).count()

#Algorithm approach

OnlineKMeans - recombining partial solutions

StreamingOnlineKmeans - partition data by examining what center the points are closest to initially for each RDD from the DStream and then run online

ARTKmeans - recompute min and max on each new RDD and recombine previous solutions
