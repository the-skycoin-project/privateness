# privateness

## Building from source

### Make Depends

* golang

### Sync go dependencies

```
go mod vendor -v
go get github.com/skycoin/skycoin@develop
go get github.com/mattn/go-colorable@v0.0.9
```

### Build the privateness binary

```
cd cmd/privateness
go build .
mv privateness ../../
cd ../..
```

### Run Privateness
```
./privateness -gui-dir=src/gui/static/ -enable-all-api-sets=true -enable-gui=true -log-level=debug
```

## Rebuilding the frontend
```
cd src/gui/static
npm ci
npm run build
```
