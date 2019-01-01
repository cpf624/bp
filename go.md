<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Golang](#Golang)
	- [godoc](#godoc)
	- [Introduction](#introduction)
	- [IDE](#ide)
		- [SublimeText](#sublimetext)
	- [Package Manager](#package-manager)
	- [Logger](#logger)
	- [Serialization](#serialization)
	- [Crypto](#crypto)
	- [Database Driver](#database-driver)
		- [MySQL](#mysql)
		- [SQLite](#sqlite)
	- [ORM](#orm)
	- [Router](#router)
	- [Web Framework](#web-framework)

<!-- /TOC -->

# Golang

### godoc
```shell
# http://localhost:8080
godoc -http=:6060

godoc fmt Printf
```

### Introduction
- [astaxie/build-web-application-with-golang](https://github.com/astaxie/build-web-application-with-golang/blob/master/zh/preface.md)
- [Awesome Go](https://awesome-go.com/)

### IDE
##### SublimeText
- install GoSublime
```shell
cd ~/Library/Application Support/Sublime Text 3/Packages
git clone https://margo.sh/GoSublime
```
- GoSublime Settings
```json
{
    "env": {
        "GOPATH": "/home/arsham/Projects/Go:/usr/bin/go",
        "PATH": "/home/arsham/Projects/Go/bin:$PATH:/usr/bin",
    },
    "comp_lint_enabled": true,
    "ipc_timeout": 2,
    "fmt_cmd": ["goimports", "-srcdir", "$_dir"],
    "on_save": [
        {"cmd": "gs_comp_lint"},
    ],
    "comp_lint_commands": [
        {"cmd": ["go", "build", "-i"]},
        {"cmd": ["golint $_fn"], "shell": true},
        {"cmd": ["go", "vet"]},
        {"cmd": ["goconst $_dir"], "shell": true},
        {"cmd": ["usedexports $_dir"], "shell": true},
        {"cmd": ["ineffassign $_fn"], "shell": true},
    ],
}
```
- [Streamline Your Sublime Text + Go Workflow](https://www.alexedwards.net/blog/streamline-your-sublime-text-and-go-workflow)
- [Supercharge your sublime text for #golang development](https://medium.com/@arshamshirvani/super-charge-your-sublime-text-for-golang-development-3239d9c376bb)

### Package Manager
- [gopm](https://github.com/gpmgo/gopm)
- [dep](https://github.com/golang/dep)
- [govendor](https://github.com/kardianos/govendor)

### Logger
- [seelog](https://github.com/cihub/seelog)
- [logrus](https://github.com/sirupsen/logrus)

### Serialization
- [json-iterator](https://github.com/json-iterator/go)
- [thrift-iterator](https://github.com/thrift-iterator/go)

### Crypto
- [scrypt](https://godoc.org/golang.org/x/crypto/scrypt)

### Database Driver
- [Go database/sql tutorial](http://go-database-sql.org)
- [SQLDrivers](https://github.com/golang/go/wiki/SQLDrivers)
##### MySQL
- [https://github.com/go-sql-driver/mysql](https://github.com/go-sql-driver/mysql) 支持database/sql，全部采用go写
- [https://github.com/ziutek/mymysql](https://github.com/ziutek/mymysql) 支持database/sql，也支持自定义的接口，全部采用go写
- [https://github.com/Philio/GoMySQL](https://github.com/Philio/GoMySQL) 不支持database/sql，自定义接口，全部采用go写
##### SQLite
- [https://github.com/mattn/go-sqlite3](https://github.com/mattn/go-sqlite3)

### ORM
- [xorm](https://github.com/go-xorm/xorm)
- [gorm](https://github.com/jinzhu/gorm)

### Router
- [Radix tree](https://en.wikipedia.org/wiki/Radix_tree)
- [httprouter](https://github.com/julienschmidt/httprouter)

### Web Framework
- [Beego](https://github.com/astaxie/beego)
- [Gin](https://github.com/gin-gonic/gin)
- [Revel](https://revel.github.io/)
- [Echo](https://echo.labstack.com/)
