# USAGE

```
go build .

./stringsvc -listen=:8001 &
./stringsvc -listen=:8002 &
./stringsvc -listen=:8003 &

./stringsvc -listen=:8080 -proxy=localhost:8001,localhost:8002,localhost:8003

```

then you can run
```
for s in foo bar baz ; do curl -d "{\"s\":\"$s\"}" localhost:8080/uppercase; done
```

to see in action.
