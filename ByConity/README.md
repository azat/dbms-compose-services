[ByConity](https://github.com/ByConity/ByConity)

ByConity is a fork of ClickHouse, with some changes, in particular:

- it does not have some new features/optimizations since it was a fork of
  ClickHouse (21.8).
- it supports transactions
- this setup uses HDFS

Note, that almost all setup was copied from the [ByConity repository](https://github.com/ByConity/ByConity/tree/master/docker/local-deploy),
and I did some modifications to use pre-built images.
