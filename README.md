# socat23

[socat](http://www.dest-unreach.org/socat/) with OpenSSL version 2 & 3 support.

_Repo for the gist I originally had [here](https://gist.github.com/leonjza/9af3ade91420ed48c6f048563885940a)._

## installation

Run the `build.sh` script, tested on Kali Linux. Alternatively, build the docker container with `docker build -t socat23 .`.

## usage

Installation using the `build.sh` script on Kali Linux will provide a new `socat23` command to use. For the docker image, example invocation would be:

```bash
docker run --rm -p 50000:80 socat23:latest socat -v -ls tcp4-listen:80,fork,reuseaddr ssl:www.google.com:443,verify=0
```
