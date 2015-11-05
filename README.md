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

Running the container
----------------------
```
docker run nyxcharon/docker-consul-backup-s3 -h consul.server -p 8500 -b s3://somebucketname
```

To provide AWS credentials mount your .aws folder and/or set your environment
variables as needed. If you are running this inside ec2 this won't be needed
if the instance has the correct permissions to access s3.

```
docker run  -v ~/.aws:/root/.aws nyxcharon/docker-consul-backup-s3 -h consul.server -p 8500 -b s3://somebucketname
```
