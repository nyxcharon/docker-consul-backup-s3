# docker-consul-backup-s3
Docker container to backup consul and upload it to s3

Info/Usage
-----

```
Backups consul to a s3 bucket. You must provde all 3 arguments

Usage: consul-backup -h CONSUL_HOST -p CONSUL_PORT -b s3://somebucketname
Usage: consul-backup -h CONSUL_HOST -p CONSUL_PORT -b s3://somebucketname/somefolder

-h | --host     - The Consul Host
-p | --port     - The Consul Port
-b | --s3bucket  - The s3 bucket path to use
```
