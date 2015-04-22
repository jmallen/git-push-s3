git-push-s3
===========

If you've ever hosted a static website from an s3 bucket you've probably wanted
an easy way to push changes to the bucket. I wanted something as simple as 
possible. 


    $ git push-s3 <yourbucketname>


What it does
============

For every path in your repo (that isn't prefixed by ".git") git-push-s3
checks to see if an s3 key exists. If it does, git-push-s3 computes the md5
sum of the local file and checks it against the corresponding file in s3. If
they differ the local file is uploaded. If the file does not exist in the bucket
then the file is uploaded as well. No files or keys are ever deleted.



Installation:
=============

Ensure you have "boto" installed, and then place git-push-s3 somewhere in your 
path (eg /usr/local/bin/).





