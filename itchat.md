Python itchat模块应用接口访问微信通知
代码如下：
```

from flask import Flask
import itchat
from itchat.content import *
import time
import re

itchat.auto_login(hotReload=True)
app = Flask(__name__)


@app.route('/')
def hello_world():
    itchat.send('访问了8080', toUserName='filehelper')
    return 'Hello World!'


if __name__ == '__main__':
    app.run(port=8080,debug=True)
```
