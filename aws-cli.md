# Using the AWS CLI with OSN

## Install the AWS CLI utility
[Official instructions to install](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) the lastest AWS command line interface 

After installing the AWS CLI, create a  "config" file, `~/.aws/config`, with
```
[yourprofilename]
output=json
```

and add a corresponding credentials entry in your "credentials" file, `~/.aws/credentials`, with
```
[yourprofilename]
aws_secret_access_key = your_secret_key
aws_access_key_id = your_access_key
```

Your profile name is the one listed on the OSN storage page, with project ID+name.  For example:
```
XYZ123415_Bob_Smith
```

After loading your `aws-cli` environment, you can use s3 commands such as:
```
aws s3 ls <yourbucket> --profile <yourprofilename> --endpoint <yourendpoint> --recursive --human-readable --summarize
```





