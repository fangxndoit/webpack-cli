# 多页面webpack脚手架
用于简单的多页网页开发，不同于vue那种单页面开发，主要有 jqury axios wx-jsk，sass，swiper如需使用其他js 通过npm 下载，模块化引入即可，也可以直接通过CDN引入。应用常景，基本多页网页开发都可以，app pc 公众号开发。
（本项目根据github网上进行了一定修改，仅供个人参考学习）

## Build Setup

``` bash
# 安装依赖
npm install

# 开发的时候在本地启localhost:8080，并开始热加载
npm run dev

# production的发布时打包
npm run build

```


## 目录结构

```

└─src                                      // src 文件夹
│    ├─pages                               // 页面文件夹
│    │  ├─mall
│    │  │      mall.html
│    │  │      mall.js
│    │  │      mall.scss
│    │  │
│    │  └─home
│    │          index.html
│    │          index.js
│    │          index.scss
|    ├─common                       // 公共css/iconfont
|    |
|    ├─images                       // 图片
│    │
│    └─tools                        // 工具文件夹
│            utils.js
|            request.js             // axios 配置
|            wx-jsdk.js             // 微信 jssdk 配置
|            wx-pay.js              //  微信支付配置
│
│  .babelrc                         // babel的配置文件
│  .eslintignore
│  .eslintrc.js                     // eslint的配置文件
│  .gitignore
│  package.json
│  page.config.js                   // 页面的配置文件
│  README.md
│  webpack.config.dev.js            // 开发环境的webpack配置文件
│  webpack.config.prod.js           // 生成环境的webpack配置文件
|  dist                             // 打包后的文件

```

## 开发流程

如果增加新页面

1. 在pages中新增一个文件夹
2. 在page.config.js中添加这个页面的信息即可

比如
```
  {
    name: 'contact',
    html: 'contact/contact.html',
    jsEntry: 'contact/contact.js'
  }
