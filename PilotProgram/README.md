# Caravan Insurance Regression

Implementation of Logistic regression in Spark and Scala.

## Running the code
```bash
$ spark-shell caravan_logistic_regression.scala
```

## Results

The results of the prediction looked bad. So, I took a look at how the label was distributed and this is what I found.
```bash
scala> df.groupBy("CARAVAN").count().select("*").show()
+-------+-----+
|CARAVAN|count|
+-------+-----+
|      0| 9236|
|      1|  586|
+-------+-----+
```