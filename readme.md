## 这是什么

这个项目主要是为了便于生成 Twikoo、Artalk、Waline 评论的表情包。。



## 如何使用

在artalk的配置文件中，配置表情包地址如下：

```yaml
# 前端配置
frontend:
  # 表情包
  emoticons: "https://cdn.jsdelivr.net/gh/SakurajimMai/emotion_generate/dist/artalk.json"
```

## 直接使用此项目的文件



关于此项目的产物参考`src/config.js`文件。

例如 阿鲁表情包的配置如下：

```
[
  {
    "name": "阿鲁",
    "path": "aru",
    "prefix": "aru-",
    "baseUrl": "https://cdn.jsdelivr.net/gh/SakurajimMai/emotion_generate/dist/aru/image",
    "twikoo": {
      "name": `阿鲁`
    },
    "artalk": {
      "name": `阿鲁`
    }
  }
]
```



那么远程链接使用的对应文件路径如下：

```
https://cdn.jsdelivr.net/gh/SakurajimMai/emotion_generate/dist/aru/valine.json
https://cdn.jsdelivr.net/gh/SakurajimMai/emotion_generate/dist/aru/artalk.json
https://cdn.jsdelivr.net/gh/SakurajimMai/emotion_generate/dist/aru/twikoo.json
https://cdn.jsdelivr.net/gh/SakurajimMai/emotion_generate/dist/aru/discuss.json
https://cdn.jsdelivr.net/gh/SakurajimMai/emotion_generate/dist/aru/info.json // waline 寻找 info.json 文件
```



> `https://cdn.jsdelivr.net/gh/SakurajimMai/emotion_generate/dist/aru`此域名为我个人的静态服务绑定的域名。

## 自己使用



1. ~~为此项目点个 Star~~，然后 fork 此项目

2. 将你的图片按照我的格式放入`src/image`目录下

3. 调整`src/config.js`文件，然后运行`src/index.js`脚本即可（或者 `npm run build`）。

   > 在`windows`系统下运行会无法将图片复制到产物目录。

4. 接下来将会生成`dist`目录，将其作为静态资源部署即可。
