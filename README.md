# 小小榫卯匠儿童交互教学网页

这是一个面向 7-10 岁儿童的榫卯线上预习教学网页。孩子可以在手机上依次完成 5 个关卡，通过视频区域、知识说明和互动练习，提前理解榫卯结构，为后续线下木作实践做准备。

## 发布文件结构

上传到 GitHub Pages 或 Netlify 时，请让仓库根目录保持下面的结构：

```txt
index.html
style.css
script.js
README.md
assets/
  images/
  videos/
    README.md
```

不要上传外层 `outputs` 文件夹，也不要让首页变成 `outputs/index.html`。

## 如何替换图片

图片放在：

```txt
assets/images/
```

请保持同名文件：

```txt
tenon.jpg
mortise.jpg
straight-joint.jpg
cross-joint.jpg
dovetail.jpg
shoulder-joint.jpg
```

后续只要替换这些同名图片，网页会自动更新。所有图片路径都是相对路径，不使用 `C:/`、`D:/` 这类本地路径。如果图片缺失，页面会显示灰色占位卡片，不会崩溃。

## 如何替换视频链接

本发布版不把大型视频文件放进仓库。请先把视频上传到 Kivicube、B站、网盘直链、腾讯云、七牛云等平台，然后打开 `script.js` 文件顶部，替换这 5 个变量：

```js
const lesson1VideoUrl = "";
const lesson2VideoUrl = "";
const lesson3VideoUrl = "";
const lesson4VideoUrl = "";
const lesson5VideoUrl = "";
```

示例：

```js
const lesson1VideoUrl = "https://example.com/lesson1.mp4";
```

如果视频链接为空，网页会显示：

```txt
视频加载中，请稍后替换视频链接
```

不会影响后续互动题和关卡流程。

## 如何开启 GitHub Pages

1. 进入 GitHub 仓库页面。
2. 点击 `Settings`。
3. 点击左侧 `Pages`。
4. `Source` 选择 `Deploy from a branch`。
5. `Branch` 选择 `main`。
6. `Folder` 选择 `/root`。
7. 点击 `Save`。

开启后，GitHub Pages 网址通常是：

```txt
https://你的用户名.github.io/仓库名/
```

例如：

```txt
https://xuyicen85-debug.github.io/sunmao-mobile-teaching/
```

## 如何用 Netlify 拖拽上传

1. 打开 Netlify 并登录。
2. 进入 Sites 页面。
3. 选择手动部署或拖拽上传。
4. 把本发布文件夹拖进去。
5. 等部署完成后，Netlify 会生成一个手机可打开的网址。

## 如何用生成的网址制作二维码

部署成功后，复制 GitHub Pages 或 Netlify 生成的网址，然后用任意二维码生成工具制作二维码。

如果网址以后变化，只需要用新网址重新生成二维码即可。
