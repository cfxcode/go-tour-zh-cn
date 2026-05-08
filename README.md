# Go 语言之旅 中文版

`A Tour of Go` 的中文化版本，包含中文课程内容、示例说明、前端界面和运行提示。

## 来源

本项目基于 Go 官方 website 仓库修改：

- 原仓库：<https://github.com/golang/website>
- 官方镜像：<https://go.googlesource.com/website>
- Tour 页面和前端资源：`_content/tour/`
- Tour 本地启动入口：`tour/`
- Tour 服务端逻辑：`internal/tour/`

说明：`tour/` 是上游 `golang.org/x/website` 仓库自带目录，不是运行命令生成的。早期的 `golang.org/x/tour` 现在主要提供练习辅助包，例如 `pic`、`reader`、`tree`、`wc`。

中文内容参考：

- <https://github.com/Go-zh/website>
- <https://github.com/Go-zh/tour>

## 启动

需要先安装 Go 和 Git。

```bash
git clone https://github.com/cfxcode/go-tour-zh-cn.git
cd go-tour-zh-cn
go mod download
cd tour
go run . -http=127.0.0.1:3999 -openbrowser=false
```

打开：

```text
http://127.0.0.1:3999/tour/
```

如果已经有本地代码：

```bash
cd go-tour-zh-cn/tour
go run . -http=127.0.0.1:3999 -openbrowser=false
```

端口被占用时换端口：

```bash
go run . -http=127.0.0.1:4000 -openbrowser=false
```

## 验证

```bash
go test . ./internal/tour ./tour
```

## 许可证

保留上游 Go 项目许可证，见 [LICENSE](LICENSE) 和 [PATENTS](PATENTS)。
