### 预览

1. 使用PDF Embed API实现[简历预览](https://docs.google.com/viewer?url=https://github.com/Kang-Jay/KangJay/raw/resume/Resume.pdf&embedded=true )
2. 通过[Github Pages](https://kang-jay.github.io/KangJay/)实现简历预览

(预览若有未渲染成功的情况, 请刷新或重新进入链接)

### 下载

访问Github链接[下载简历](https://github.com/Kang-Jay/KangJay/raw/resume/Resume.pdf)

<br><br>



### 实现方法

#### 预览

1. 使用PDF Embed API, 依赖于Google Docs Viewer.

   在markdown中嵌入以下代码:

   ```html
   <iframe src="https://docs.google.com/viewer?url=https://github.com/Kang-Jay/KangJay/raw/main/Resume.pdf&embedded=true" style="width:100%; height:1100px;" frameborder="0"></iframe>
   ```

2. 在PDF Embed API基础上借用Github Pages, 创建仓库并建立index.html. 

   在html中嵌入以下代码:

   ```html
   <iframe src="https://docs.google.com/viewer?url=https://github.com/Kang-Jay/KangJay/raw/main/Resume.pdf&embedded=true" style="width:100vw; height:100vh;" frameborder="0"></iframe>
   <style>
       body{
           margin: 0;
       }
   </style>
   ```

   形成与第一种方法类似的效果. 如果想要做其他更改可以自己撰写html文件.

#### 下载

Github上创建仓库, 设置分支, 上传PDF文件, 按照以下格式访问对应链接:

```txt
https://github.com/<user-name>/<repo>/raw/<branch>/<path-to-pdf>.pdf
```

