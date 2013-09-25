StorNode
========

StorNode, is a Bitcoin based Pay-to-Filehost web service. It is coded in [Python](http://python.org/) and  [Flask](http://flask.pocoo.org/), a Python microframework for web. It is designed to run on a Linux based VPS. [Digital Ocean](http://digitalocean.com) or [Ramnode](http://www.ramnode.com/) are recommended.


----------


Users and developers want to be able to store their files and data on the web. Users typically use services like Google Drive or Dropbox, while developers typically use a service like Amazon S3. These services require their users to sign-up, have data storage limits (after which they can be quite expensive), don't allow for easy automation, and don't allow direct access to files. 

The idea is simple: A Bitcoin based Pay-to-Filehost web service that allows anyone to upload files via a web interface or API. The user then will pre-pay the service to cover the cost of hosting the files.  This payment will be made in Bitcoin, and is priced based on size of the file, bandwidth required, and the duration that the file has been hosted. When the account balance is 0, the files will be queued for deletion. 

See [https://bitfetch.com/](https://bitfetch.com/) for design ideas. 

Sample User Interaction
-------
1. The user wants to store a video file on the web to share.
2. The user uploads the file to StorNode using the web interface.
3. The user is presented with rates based on bandwidth usage, file size, and duration of hosting. 
4. The user makes a micro-payment to StorNode. After the payment is received, StorNode will allow the file to be used/download. The account balance will be charged as the file is used/downloaded. 
5. The user is allowed to freely use/download the file until the account balance is 0. 
