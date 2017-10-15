#loggly-s3-sources

"Fork" of [https://www.loggly.com/install/SQS3script.py](https://www.loggly.com/install/SQS3script.py)

####Documentation:

- Loggly: [Amazon S3 Log Ingestion](https://www.loggly.com/docs/s3-ingestion-auto/)
- AWS: [Named Profiles](http://docs.aws.amazon.com/cli/latest/userguide/cli-multiple-profiles.html)

##Dependency Management:

[pipenv](https://docs.pipenv.org/) is used for this project

To install dependencies, simply

```bash
$ pipenv install
```

To enter a virtualenv shell

```bash
$ pipenv shell
```

This will spawn a new shell where all dependencies will be present.

##Usage:

```bash
$ python SQS3script.py --s3bucket  --acnumber
```

**s3bucket**: The name of the bucket from which you would like to send logs.

**acnumber**: Your AWS account number, which you can get from your AWS account page in the console.

**user (optional)**: The IAM username that Loggly should use when accessing the queue and bucket. Please use a dedicated user for Loggly. The default is *loggly-s3-user*.

**sqsname (optional)**: The name of the SQS queue that Loggly will receive notifications from when objects are added to the bucket. Please use a dedicated queue for Loggly. The default is *loggly-s3-queue*.

**profile (optional)**: The AWS profile that will be used. The default is *default*
