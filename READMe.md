aws --version
aws-cli/2.6.3 Python/3.9.11 Linux/5.4.0-1029-gcp exe/x86_64.ubuntu.20 prompt/off
aws s3 ls

#create bucket
aws s3 mb s3://BucketNameHere

#list the bucket contents
aws s3 ls s3://BucketNameHere

#copy file to bucket
aws s3 cp /usercode/Data/index.html s3://BucketNameHere/index.html
aws s3 cp s3://BuckerNameHere/index.html /usercode/Data/index.html

#download all files from bucket
aws s3 cp s3://BucketNameHere . --recursice

#copy from one bucket to the other
aws s3 cp s3://BucketNameHere s3://NewBucketNameHere --recursive

#generrate presigned url to access s3 objects
aws s3 presign s3://BucketNameHere/index.html

#remove files
aws s3 rm s3://BucketNameHere/index.html

#remove all files
aws s3 rm s3://BucketNameHere --recursive

#remove empty bucket
aws s3 rb s3://BucketNameHere

#delete all files in the bucket
aws s3 rb s3://BucketNameHere --force
