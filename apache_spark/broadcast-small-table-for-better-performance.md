# Using Spark Broadcast to improve your join performance

Spark broadcast joins are perfect for joining a large DataFrame with a small DataFrame.

Broadcast joins cannot be used when joining two large DataFrames.

## How

*****To use it with Spark sql query**

Simply use `/*+ BROADCAST(THIS_IS_SMALL_TABLE) */`

```sql
SELECT /*+ BROADCAST(table_2) */ table_1.*, table_2.detail
FROM table_1 JOIN table_2
ON table_1.key=table_2.key
```

**To use with Spark DataFrame based**

```python
from pyspark.sql.functions import broadcast
from pyspark.sql import SparkSession


spark = SparkSession.builder.master("local").appName("Hello world").getOrCreate()
customer_df = spark.createDataFrame(
    [
        (1, 'foo', 100), # create your data here, be consistent in the types.
        (2, 'bar', 101),
    ],
    ['id', 'customer', 'location_id'] # add your columns label here
)

location_df = spark.createDataFrame(
    [
      (100, 200),
      (101, 500),
    ],
    ['location_id', 'location_name']
)

customer_location = customer_df.join(broadcast(location_df), ['location_id'])

customer_location.explain()

```

