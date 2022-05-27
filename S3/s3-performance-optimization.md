# S3 Performance Optimization

## Single PUT upload

* Single data stream to S3
* Stream fails - upload fails
* Requires full restart
* Speed & reliability = limit of 1 stream
* Any upload up to 5GB

## Multipart upload

* Data is broken up
* Min data size 100MB for multipart
* 10,000 max parts, 5MB -> 5GB
* Last part can be smaller than 5MB
* Parts can fail, and be restarted
* Transfer rate = speed of all parts

## S3 Accelerated Transfer

* Uses AWS edge locations to speed up transfer rates
