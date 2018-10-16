# Original Info from original developper:
# infping
Parse fping output, store result in influxdb 0.9
See blog post for more info https://hveem.no/visualizing-latency-variance-with-grafana


# Installation (Debian 9)

- Clone the repo
- Install golang https://golang.org/doc/install
- install packages fping
- configure GOPATH to the folder of your git cloned repo : export GOPATH=/yourfolder/infping
- from the $GOPATH folder :
	- go get "github.com/influxdata/influxdb/client"
	- go get "github.com/pelletier/go-toml"
- build : go build -o infping infping.go
- configure config.toml file
- modify infping.service (check path and user), copy to /lib/systemd/system then start/enable.
