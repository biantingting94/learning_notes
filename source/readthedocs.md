## readthedocs

### 1、安装sphinx

```brew cask install sphinx```

或

```pip install sphinx```

### 2、创建文档

文档名：Books

```cd /Users/jessica/Documents/Learning_notes```

创建工程目录：

```sphinx-quickstart```

### 3、更改conf.py文件

3.1、更改主题：

```vim source/conf.py```

```html_theme = "sphinx_rtd_theme"```

3.2、支持markdown编写：

```
from recommonmark.parser import CommonMarkParser
source_parsers = {
    '.md': CommonMarkParser,
}
source_suffix = ['.rst', '.md']
```

3.3、生成html文档

回到主目录Learning_notes:

```cd ../..```

生成html文档

```make html```

3.4、预览效果

进入build/html用浏览器打开index.html

### 4、参考

http://scottming.com/2016/03/27/readthedocs/

https://www.xncoding.com/2017/01/22/fullstack/readthedoc.html



