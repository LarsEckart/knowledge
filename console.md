# Stuff to type in your console

```
lsof | grep deleted
```

`lsof -i :8080` — find out which process is listening on port 8080

`lsof -i -s TCP:LISTEN` — find out which processes are listening at all
`lsof -i6` — show all IPv6 connections

https://medium.com/@copyconstruct/lsof-f2b224eee7b5


## ping other server in case http

```
curl --insecure -v https://www.google.com 2>&1 | awk 'BEGIN { cert=0 } /^\* Server certificate:/ { cert=1 } /^\*/ { if (cert) print }'
```
