# spark
## Getting Started
Follow these steps to get up and running with pyspark.
1. Install [spark](https://spark.apache.org/downloads.html). 
Here, we will assume you install it to `<spark-dir>`.
    1. Choose a Spark release.
    2. Choose __pre-built__ for Apache Hadoop.
2. Run `pip install pyspark findspark`
3. Add the following to your `.bashrc`:
    * `export SPARK_HOME="<spark-dir>/spark"`
    * `export PATH="$SPARK_HOME/bin:$PATH"`
4. You can either run spark in the terminal using `pyspark`,
or you can run the following in python:
```python
import findspark
import pyspark

findspark.init("<spark-dir>/spark")

sc = pyspark.SparkContext(appName="tests")
```
When you create a spark context, spark will also spin up the web UI
at [http://localhost:4040].

If at any point you decide that you are finished with spark, run
```python
sc.stop()
```

## Key concepts
See 

## Kubernetes
Needs investigating. See `~/spark/kubernetes`
