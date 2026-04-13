## 简介

- 基于 https://github.com/gin-contrib/gzip v1.2.6

### fix: gin zip中间件，涉及请求转发（forward）时，走 Content-Length 快速路径时，应该在调用底层 writer 之前就移除头部，而不是依赖 defer

![bug0.png](bug0.png)
