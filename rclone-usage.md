Commands are in the form:

```
rclone [command] OSN:/nameofbucket
```
To make it easier to follow the directions by cut/paste, define an environment variable 
with your bucket name.
```
$ export BUCKET=OSN:/XYZ123456-bucket01
```
Do a test...check what is in the bucket.
```
$ rclone ls $BUCKET 
```
Create a text file and copy it to the bucket.
```
$ echo "hello world" > hello.txt
$ rclone copy hello.txt $BUCKET

Check that the file transfer completed:
```
$ rclone ls $BUCKET
       12 hello.txt

Veryify the file's content:
```
$ rclone cat $BUCKET/hello.txt
hello world
```

