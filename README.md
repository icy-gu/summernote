# summernote
 summernote富文本编辑器

## 1、安装相关命令
``` 
    bootstrap:"4.1.1" 
    font-awesome:"4.7.0"
    jquery:"3.3.1"
    codemirror:"5.37.0"
    summernote:"0.8.10"
```

## 2、在项目中引入相关js和css
> 在index.art中引入
```
    <script src=static/js/jquery.min.js></script>
    <link href=static/js/summernote/summernote-lite.min.css rel="stylesheet" />
    <script src=static/js/summernote/summernote-lite.min.js></script>
    <link href=static/public/images/tam-emoji/css/emoji.css rel="stylesheet" />
    <script src=static/public/images/tam-emoji/js/config.js></script>
    <script src=static/public/images/tam-emoji/js/tam-emoji.js></script>
```
> 在main.hs中引入
```
import 'font-awesome/css/font-awesome.css'
```

## 3、在项目中引用组件index.vue
```
import summerNote from './index.vue'

<summer-note id="summerNote" placeholder="请输入内容" ref="summerNote"></summer-note>
```

参数|备注
--------|--------
id|组件的唯一标识
placeholder|本文框内的描述

> ## 方法
> 获取值
> ```
> this.$refs.summerNote.getContent()
> ```
> 设置值
> ```
> this.$summerNote.setContent('sssss')
> ```
