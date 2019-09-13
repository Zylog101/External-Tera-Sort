# External-Tera-Sort

The goal of this project is to gain insight into the working of data intensive applications with resource constraints. In specific working with large dataset in memory limitations

**Utilizing**
* Amazon Web Services, specifically the EC2 cloud (http://aws.amazon.com/ec2/)
* Tera byte of data

TeraSort application is implemented in Java

**Description:**
* Program sorts larger than memory datasets, which is also known as external sort. Two datasets are created, a small and a large dataset, which will be used to benchmark sorting 128GB dataset and 1TB dataset.

Datasets are generated using a generator http://www.ordinal.com/gensort.html

**Configuration used:**
* Virtual Cluster (1-node i3.large): virtual cluster of 1 node on Amazon EC2 using i3.large instance with a dataset of 128GB in size
  * Shared-Memory TeraSort implementation is of a Shared-Memory TeraSort application in Java (without using Hadoop or Spark)
  * Multi-threading is used to take advantage of multiple cores and SSD storage (which also requires multiple concurrent requests to achieve peak performance)
* Virtual Cluster (1-node i3.4xlarge): virtual cluster of 1 node on Amazon EC2 using i3.4xlarge instance with a dataset of 1TB in size
  * Shared-Memory TeraSort Implementation is of a Shared-Memory TeraSort application in Java (without using Hadoop or Spark)
  * Number of threads is increased to make optimal use of the 16-core instance
