# S3 Select and Glacier Select

* S3 can store HUGE objects (up to 5TB)
* You often want to retrieve the entire object
* Filtering at the client side doesn't reduce the data transfer
* S3/Glacier select let you use SQL like statements to select part of the object, pre-filtered by S3
* CSV, JSON, Parquet, BZIP2 compression for CSV and JSON
