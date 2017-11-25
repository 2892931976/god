# GoD 
## 功能介绍

* 完整实现(复制) golang 官方 go get 命令
* 仅针对 golang.org/x 包资源做特殊处理, 自动跳转到github.com/golang下载文件
* 会指定下载目录到正确的golang.org/x目录内
* 可完全替代官方go get 命令
* 体验与原版go get 完全一致(因为99%代码一致, 哈哈哈哈)

## 使用方法

* 安装 `go get -v -u github.com/yanjunhui/god`
* 使用方法和参数与官方 `go get` 一致, 将命令修改为 `god get`

## 无法运行
### `-bash: god: command not found`
1. 执行 `go env`, 查看 GOPATH 路径, 例如: `GOPATH="/Users/yanjunhui/go"`
2. 继续执行 `export PATH=$PATH:/Users/yanjunhui/go/bin` (将GOPATH路径修改为你实际路径)
3. linux mac windows 各系统永久添加系统变量路径方法请利用搜索引擎查找

## 示例
* 单独下载`golang.org/x`资源 `god get -v -u golang.org/x/net/ipv4`
* 下载其他第三方包,可自动解决依赖 `god get -u -v github.com/labstack/echo`


###### ps: 名字命名为 god, 仅仅是取 go download 的简称, 请宗教人士不要误会, 别打我

