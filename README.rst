===========
 aws-login
===========

Simple script for generating the aws credentials file needed by
external scripts (such as serverless).

Requires `jq <https://stedolan.github.io/jq/>`_

Note that this script assumes several things:

* An AWS account has already been created.
* `aws configure sso` has already been run

  * note that the required settings for configuring the sso are

    * sso url: https://dotorg.awsapps.com/start
    * sso region: us-east-2 (different from the accounts region which is us-west-2)
    * when prompted, log in with your gmail account
    * choose dotOrg-developer for the account you want to use for develop
    * use json as the default output format

* `aws sso logout` will not remove the credentials file.

