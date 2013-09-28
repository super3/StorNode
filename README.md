StorNode
========

StorNode, is a Bitcoin based Pay-to-Filehost web service. Coded in [Python](http://python.org/) and  [Flask](http://flask.pocoo.org/), a Python microframework for web. May run off it's own instance of [Bitcoind w/ JSON-RPC](https://en.bitcoin.it/wiki/API_reference_(JSON-RPC)) or through the [Coinbase API](https://coinbase.com/docs/api/overview). Must be run on a Linux based web server, [Debian](http://www.debian.org/) distro recommended. 

## Summary ##

Users and developers want to be able to store their files and data on the web. Users typically use services like Google Drive or Dropbox, while developers typically use a service like Amazon S3. These services require their users to sign-up, have data storage limits (after which they can be quite expensive), don't allow for easy automation, and don't allow direct access to files. 

The idea is simple: A Pay-to-Filehost web service that allows anyone to upload files via a web interface or API. The user will pre-pay the service to cover the cost of hosting the files. This payment will be made in Bitcoin, and is priced based on size of the file, bandwidth required, and the duration that the file has been hosted. These files will be served, and the update balances on the hour. When the account balance is 0, the files will be queued for deletion. 

## Sample User Interaction ##

1. The user wants to store a video file on the web to share.
2. The user uploads the file to StorNode using the web interface.
3. The user is presented with rates based on bandwidth usage, file size, and duration of hosting. 
4. The user makes a micro-payment to StorNode. After the payment is received, StorNode will allow the file to be used/download after payment is confirmed.
5. The user is allowed to freely use/download the file until the account balance is 0. 

## Recommendations ##
The follow VPS hosts where found to be suitable based on price and storage. 

- [Digital Ocean](http://digitalocean.com) - $5 Month / 512 RAM / 20 GB SSD / 1 TB Transfer **[Testing Phase]**
- [RamNode](http://www.ramnode.com/) - $2 Month (Must $24 Year) / 128 RAM / 50 GB SSD-Cached / 500 GB Transfer **[Deploy Phase]**
- [VirtualVM](http://www.virtualvm.com/) - $4 Month / ??? RAM / 40 GB Storage / 5 TB Transfer **[Bitcoin]**
- [Amazon EC2](https://aws.amazon.com/ec2/) - Possibly...




Design to follow: [BitFetch](https://bitfetch.com/).


