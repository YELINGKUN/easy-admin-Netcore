# Easy.Admin

#### 🌈 介绍（喜欢的话给个 star 吧 ❤️）

- 后端基于`.NET 9` + `Furion ` + `SqlSugar` + `Vue3` + `TypeScript` ，并且支持多种数据库
- 博客基于`Vue3` + `TypeScript` + `Vuetify` + `Pinia`,分为普通版本和 SSR（服务端渲染，支持 SEO），服务端渲染框架基于分别使用`nuxtjs`和`vite-plugin-ssr`实现

#### 📚 后端 API 使用教程

> 注意：每次修改[`applicationsettings.json`](https://gitee.com/miss_you/easy-admin/blob/master/src/backend/Easy.Admin.Application/applicationsettings.json)中的配置都需要重新生成解决方案方可生效
> 文件所在目录：`/src/backend/Easy.Admin.Application/applicationsettings.json`

1. 可根据需求修改[`applicationsettings.json`](https://gitee.com/miss_you/easy-admin/blob/master/src/backend/Easy.Admin.Application/applicationsettings.json)中的配置文件中的配置，默认使用的 sqllite 数据库，可修改数据连接字符串更改数据，修改成功后重新生成解决方案，系统会自动创建数据库和初始化基础数据
2. 附件默认上传至站点目录中，可以修改[`applicationsettings.json`](https://gitee.com/miss_you/easy-admin/blob/master/src/backend/Easy.Admin.Application/applicationsettings.json)中`OssConnection`节点，支持上传至站点目录以及常用的对象云存储（Minio、腾讯云、阿里云），使用文档：<https://github.com/oncemi/OnceMi.AspNetCore.OSS> ；如果需要使用对象云存储，需将`OssConnection`节点中的`Enable`设置为`true`
3. 缓存默认使用的内置缓存，可修改[`applicationsettings.json`](https://gitee.com/miss_you/easy-admin/blob/master/src/backend/Easy.Admin.Application/applicationsettings.json)中的`easycaching`节点；支持`In-Memory`（默认）、`Redis`、`Memcached`、`SQLite`、`Hybird`、`Disk`、`LiteDB`等；使用文档：<https://easycaching.readthedocs.io/en/latest/>

#### ⚡ 注意事项

> 运行后台管理端或者博客前请先检查本地的`node`版本；`node`版本 >= [16](https://nodejs.cn/)
>
> 博客普通版与服务端渲染版 UI 界面一致，渲染模式有所区别

#### 📚 后端管理端使用说明

> 后端管理平台默认账号密码：`admin/123456`；所在目录：`/src/frontend/admin`

```bash
# 安装依赖
pnpm install

# 运行项目
pnpm run dev

# 打包发布
pnpm run build
```

#### 📚 博客普通版使用说明（推荐服务端渲染版本）

> 项目所在目录：`/src/frontend/blog`

```bash
# 安装依赖
yarn

# 运行项目
yarn run dev

# 打包发布
yarn run build
```

#### 📚 博客服务端渲染版使用说明

> 服务渲染有两种实现方式（推荐第 2 种方式）
>
> 1、项目所在目录：`/src/frontend/vite-ssr-blog`，基于`vite-plugin-ssr`实现，官方文档：[vite-plugin-ssr](https://cn.vite-plugin-ssr.com/)
>
> 2、项目所在目录：`/src/frontend/blog-nuxt`,基于`nuxtjs`实现，官方文档：[Nuxt](https://nuxt.com/)

```bash
# 安装依赖
yarn

# 运行项目
yarn run dev

# 打包发布
yarn run build
```
