# [原神抽卡点名器](https://genshin.jerryz.com.cn/)
![原神点名器](https://stats.deeptrain.net/repo/cyanial/genshin-impact-picker/?theme=light)

[![Release](https://github.com/cyanial/genshin-impact-picker/actions/workflows/release.yml/badge.svg)](https://github.com/cyanial/genshin-impact-picker/actions/workflows/release.yml)[![Pages](https://github.com/cyanial/genshin-impact-picker/actions/workflows/page.yml/badge.svg)](https://github.com/cyanial/genshin-impact-picker/actions/workflows/page.yml)[![Build app](https://github.com/cyanial/genshin-impact-picker/actions/workflows/app.yml/badge.svg)](https://github.com/cyanial/genshin-impact-picker/actions/workflows/app.yml)

## 公共站点

[genshin.jerryz.com.cn](https://genshin.jerryz.com.cn/)

## Note

[![发布状态](https://github.com/cyanial/genshin-impact-picker/actions/workflows/release.yml/badge.svg)](https://github.com/cyanial/genshin-impact-picker/actions/workflows/release.yml) [![页面状态](https://github.com/cyanial/genshin-impact-picker/actions/workflows/page.yml/badge.svg)](https://github.com/cyanial/genshin-impact-picker/actions/workflows/page.yml) [![应用构建状态](https://github.com/cyanial/genshin-impact-picker/actions/workflows/app.yml/badge.svg)](https://github.com/cyanial/genshin-impact-picker/actions/workflows/app.yml)

## 注意

> 感谢 [Genshin-Impact-Wish-Simulator](https://github.com/Mantan21/Genshin-Impact-Wish-Simulator) 作者的[批准](https://github.com/Mantan21/Genshin-Impact-Wish-Simulator/issues/95)。

## 使用方法

>以下任一方式完成后，请查看[配置教程](http://docs.mznet.pro/users/configure)

### 应用程序(推荐)

从[github release](https://github.com/cyanial/genshin-impact-picker/releases/latest)中按照发行说明来获取对应系统的程序包即可

### 公共站点

> 尽量先使用应用程序，站点可能存在网络波动

> 欢迎大家在不影响正常使用的情况下，分享自己部署的点名器站点，以供大家共同使用：

1. [dm.mznet.pro](https://dm.mznet.pro)
  > 本站点使用Cloudflare减速器，可能会有一定的访问延迟，请保持耐心。我将尽力保持长期运营。
2. [genshin.jerryz.com.cn](https://genshin.jerryz.com.cn/)
3. [demo-picker.shawn404.top](https://demo-picker.shawn404.top)

更多的公共站点可在[文档：公共站点](http://docs.mznet.pro/users/public)中查看

## 更多

更多的使用方法及开发文档可在[这里](http://docs.mznet.pro)查看

## 许可证

本项目采用 `CC BY-NC-SA 4.0` 许可证，不得用于商业用途。

### 原仓库许可证：WishSimulator（MIT 许可证）

```
MIT License

Copyright (c) 2022 WishSimulator

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
## Star History

### 打包exe

#### Electron

在 `Genshin-Impact-Wish-Simulator` 中执行

```bash
$ npm run build
```

将生成的静态文件 `.vercel/static` 拷贝到 `electron-static/static` 目录中, 覆盖掉.

进入 `electron-static` 目录执行

```bash
$ npm install
$ npm run build (生成当前系统可执行文件)
$ npm run build-win (生成win32-x64)
```

#### Tauri

使用Tauri打包的体积较小，因为其调用系统webview，打包体积可减少200-300M  127M(tauri打包)  418M(electron打包)

> ps: tauri由于调用系统webview，因此不支持win10以下的系统，但可通过配置文件内置webview解决，具体见：https://tauri.app/zh-cn/v1/guides/building/windows 的`Supporting Windows 7`这一部分

在 `Genshin-Impact-Wish-Simulator` 中执行

```bash
$ npm run tauri build
```

### Deploy with Netlify

通过本按钮可直接一键部署至Netlify（本仓库已内置配置文件，**懒人专用**）

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/cyanial/genshin-impact-picker&base=Genshin-Impact-Wish-Simulator)


### Deploy with Vercel

网页版：[genshin.jerryz.com.cn](https://genshin.jerryz.com.cn/)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/cyanial/genshin-impact-picker)

部署成功后，点击 `Settings-General` , 将 `Build & Development Settings` 下的 ~~`Output Directory` 设置为 `.vercel/static`，(Vercel自己会设置的)~~ 将 `Root Directory` 设置为 `Genshin-Impact-Wish-Simulator`。回到 `Deployments` 下，点击当前部署最右侧的三个点，选择 `Redeploy`，等待部署完成后访问 Vercel 提供的域名即可使用。
