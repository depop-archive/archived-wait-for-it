# IMPORTANT
This relies on a bash shell, without this you cannot utilise this utility.
If you are using alpine container builds then add bash

```apk add bash```


# WHY bash?

Well we could netcat, but then we're stuck in sh shell hell where we have to use dynamic variable names for arrays.

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
