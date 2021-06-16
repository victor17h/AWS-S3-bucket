# S3 commands to interact between local machine and AWS

## Access instance

- Be in ~/.ssh
- ssh into the instance created

## Inside the instance

- `sudo apt-get update -y`
- `sudo apt-get install python`
- `python` (to check if installed)
- `sudo apt-get install python-pip`
- `sudo apt-get install awscli`
- `aws configure`
- Insert the following information (ID and key provided in excel):
		- Access key ID
		- Secret access key
		- eu-west-1
		- json
- `aws s3 ls`
- `aws s3 mb s3://devops-bootcamp-victor-bucket` to create the bucket
- `sudo nano devops_bootcamp_test.txt` to create a file
- `ls` to check if created
- `aws s3 cp devops_bootcamp_test.txt s3://devops-bootcamp-victor-bucket/`, first the file that wants to be send and then the destination bucket
- Check in AWS buckets if the file is in the bucket created
- `sudo rm devops_bootcamp_test.txt` to remove the file from local machine
- `aws s3 sync s3://devops-bootcamp-victor-bucket/devops_bootcamp_test.txt`, to import the file from S3 to your machine
- `ls` to check if it worked
- `aws s3 rm s3://devops-bootcamp-victor-bucket/devops_bootcamp_test.txt` to remove the file from the bucket
- `aws s3 rb s3://devops-bootcamp-victor-bucket` to delete the bucket
