# Original Info from original developper:
# infping
Parse fping output, store result in influxdb 0.9
See blog post for more info https://hveem.no/visualizing-latency-variance-with-grafana


# Installation (Debian 9)

- Create a dedicated user, like infping for example.
- Clone the repo, and correct rights to infping user/group.
- Install golang https://golang.org/doc/install
- Install package fping
- Configure GOPATH to the folder of your git cloned repo : export GOPATH=/yourfolder/infping
- From the $GOPATH folder :
	- go get "github.com/influxdata/influxdb/client"
	- go get "github.com/pelletier/go-toml"
- Build : go build -o infping infping.go
- Configure config.toml file
- Modify infping.service (check path and user), copy to /lib/systemd/system then start/enable.
