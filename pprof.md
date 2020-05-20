## pprof 安装及使用
### golang pprof 用于对线上运行程序 性能监控与分析

### 工具安装

```
go get -u github.com/google/pprof
```

### 代码注入

```
import _ "net/http/pprof"
```

### 启动服务(6060端口为例)

```
go run ...
```

### 获取监控文件(heap为例)

```
curl http://localhost:6060/debug/pprof/heap > heap.profile
```


### pprof web监控示例

```
pprof -http=: ./heap.profile
```

## more
### [pprof tools](https://golang.org/pkg/net/http/pprof/)
### [pprof doc](https://github.com/google/pprof)
### [xxjwxc doc](https://xxjwxc.github.io/post/pprof/)
