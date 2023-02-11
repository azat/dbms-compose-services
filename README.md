### Intro

A set of `docker-compose` services for various DBMS.

### Usage

Simply go into some subfolder, and run `make`, this will start required nodes
and spawn client.

```sh
cd starrocks
make
```

### Implementation

- Each DBMS container SHOULD use bind mount for storage and logs
- Each DBMS container SHOULD expose server ports
- Each DBMS container SHOULD use host names over IP addresses (if it is possible)
- Each DBMS container SHOULD use bind mount for /root (to preserve history files)
