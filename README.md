# WLA - wlfcss - line accelerate

使用 [淘宝 NPM 镜像](https://developer.aliyun.com/mirror/NPM) 加速包管理工具安装依赖的速度。

---
## 介绍

**通过环境变量令 npm、npx、yarn、pnpm、pnpx、nvm、 node-sass、Electron、Puppeteer、Cypress、Sharp 等包使用淘宝镜像安装。**

> 本工具有效解决依赖的依赖不经过淘宝源的问题
{.is-success}

> 本工具对包管理工具本身零侵入，同时，对环境变量的设置也是一次性的，并不会产生任何的副作用，请放心使用。
{.is-success}

## 安装

```bash
yarn global add wla
```

## 使用

**对于常用的包管理命令，`wla` 提供了使用淘宝 NPM 镜像的等价命令，除了发布包到 npm 时必须使用 `npm publish` 外，都可以使用等价命令进行相关操作：**

| 原命令 | 使用淘宝 NPM 镜像的命令 | 示例                  |
| ------ | ----------------------- | --------------------- |
| `nvm`  | `wnvm` (或 `wla nvm`) | `wnvm install 8.0.0`  |
| `npm`  | `wnpm` (或 `wla npm`) | `wnpm install react`  |
| `npx`  | `wnpx` (或 `wla npx`) | `wnpx kill-port 3000` |
| `yarn` | `wyn` (或 `wla yarn`) | `wyn add react`       |
| `pnpm` | `wpm` (或 `wla pnpm`) | `wpm add react`       |
| `pnpx` | `wpx` (或 `wla pnpx`) | `wpx kill-port 3000`  |

**对于其他命令，在使用时加上 `wla` 前缀即可，比如：**

```bash
wla printenv npm_config_registry
# -> https://r.npm.taobao.org
```

## 感谢

**本项目参考阿里开源项目：https://github.com/yiminghe/tyarn**
