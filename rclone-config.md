# Configure Rclone for OSN access

First, determine where rclone wants to store its config file for your OS / installation type.

```
 $ rclone config file
Configuration file doesn't exist, but rclone will use this path:
/home/$USER/.config/rclone/rclone.conf
```
Now, open up the /path/to/rcloneconfig/rclone.conf in a text editor and populate the config file.

```
[OSN]
type = s3
provider = Ceph
access_key_id = <access key here>
secret_access_key = <secret key here>
endpoint = https://mghp.osn.xsede.org
no_check_bucket = true
```

The name between the [] is descriptive and will be used in rclone commands to refer to your
storage. The access_key_id and the secret_access_key should have been provided to you
or are available in OSN Storage Portal.


