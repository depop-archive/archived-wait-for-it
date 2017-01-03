# IMPORTANT
This relies on NETCAT, without this you cannot utilise this utility.

```apt-get install netcat```

or

```apk add netcat-openbsd```


# WHY netcat?

We should netcat because the binary is considerably smaller than bash, and so it will work inside alpine

## Usage

```
wait-for-it.sh host:port [host:port] [-t timeout] [-- command args]
-t TIMEOUT                  Timeout in seconds, zero for no timeout
-- COMMAND ARGS             Execute command with args after the test finishes
```


## Example
```
./wait-for-it.sh www.google.com:80 www.yahoo.com:80 -t 5 -- echo "hello world"
Connection to www.google.com port 80 [tcp/http] succeeded!
Connection to www.yahoo.com port 80 [tcp/http] succeeded!
hello world
```
