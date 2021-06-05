## 1. go mod tidy - timeout

> ➜  hello go mod tidy
> go: finding module for package rsc.io/quote
> ^@example.com/hello imports
> 	rsc.io/quote: module rsc.io/quote: Get "https://proxy.golang.org/rsc.io/quote/@v/list": dial tcp 172.217.27.145:443: i/o timeout

https://goproxy.io/zh/		
https://goproxy.io/zh/docs/getting-started.html		
https://goproxy.io/zh/docs/GoLand-configuration-goproxy.html		

- 临时设置：

```bash
# 配置 GOPROXY 环境变量
export GOPROXY=https://goproxy.io,direct
# 还可以设置不走 proxy 的私有仓库或组，多个用逗号相隔（可选）
export GOPRIVATE=git.mycompany.com,github.com/my/private
```

- 使配置长期生效：

```shell
# 设置你的 bash 环境变量
echo "export GOPROXY=https://goproxy.io,direct" >> ~/.profile && source ~/.profile

# 如果你的终端是 zsh，使用以下命令
echo "export GOPROXY=https://goproxy.io,direct" >> ~/.zshrc && source ~/.zshrc
```

