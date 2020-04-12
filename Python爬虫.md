### 1、Python直接打开浏览器

```python
import webbrowser
webbrowser.open('http://www.baidu.com')
```

![](\picture\fig1baidu.png)

### 2、使用Requests包获取网页的内容

```powershell
pip3 install requests -i https://pypi.tuna.tsinghua.edu.cn/simple
```

```python
import requests
content = requests.get('https://www.baidu.com')
content.status_code
```

content是一个Response对象

```python
content.text
```

### 基本的HTML的结构、爬虫

```html
<html>
    <head>
        
    </head>
    
    <body>
        <div>
        <h1>
        Test h1 
        </h1>
           <h2>
               Test h2
            </h2>
            <script>
            var x = 10;
            var y = 20;
                document.write(x);
                document.write(y);
            if (x>20){
                alert("x>20");
            }else{
                alert("x<20");
            }
            </script>
        </div>
    </body>
</html>
```

### Regular Expression 正则表达式

```python
import re
```

判断一下电话号码或者邮政编码：

NNN-NN-NNNNNNNNN（N表示数字）

1、长度是16位

判断086-47-222222221是不是电话号码？
