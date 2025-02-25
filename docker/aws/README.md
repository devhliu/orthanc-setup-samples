# Purpose

This is a sample setup to demonstrate how to run an Orthanc in AWS and persist the data inside an AWS PostgreSQL RDS database and an S3 bucket.

# Prerequisites

## S3 Storage

- Create a S3 bucket in AWS Console (i.e: `test-orthanc-s3-plugin`).
- Get the ACCESS_KEY and SECRET_KEY of a user with read/write/delete access to this bucket.
- Copy the SECRET_KEY in `aws-s3-secret-key.txt` file
- Update the environment variables in the docker-compose.yml with the BucketName, Region and AccessKey

## SQL Database

- Create a new RDS or Aurora SQL Database (i.e: `yourdb`)
- In the `network` section, make sure the VM running Orthanc will have access to that DB server.
- Update the environment variables in the docker-compose.yml with the Hostname, Username, Port and Database.  
  Note that the Database name might actually be empty !
- Copy the password in the `rds-password.txt` file 


# Starting the setup

To start the setup, type: `docker-compose up -d` and `docker-compose logs` to access the logs later on.

# demo

Orthanc is accessible on [http://localhost:8042](http://localhost:8042).  If you upload data to Orthanc,
everything will be stored in the AWS cloud.
