- 查看npm版本

  ```
  $ npm -v
  ```

- 更新npm至最新版本

  ```
  $ sudo npm install npm@latest -g
  ```

- 安装依赖至生产环境，如vue、react等

```
$ npm install --save  (-S)
```

¨安装依赖至开发环境，比如gulp、webpack、babel等，一般是辅助工具。

```
$ npm install --save-dev  (-D)
```

- 淘宝镜像命令

  淘宝 NPM 镜像是一个完整 npmjs.org 镜像，你可以用此代替官方版本(只读)，同步频率目前为10分钟一次，以保证尽量与官方服务同步。

  你可以使用淘宝定制的 cnpm (gzip 压缩支持) 命令行工具代替默认的 npm:

  ```
  npm install -g cnpm --registry=https://registry.npm.taobao.org
  ```

- 使用npm安装模块

  ```
  npm install <module name>
  ```

  例如：用npm安装常用的Node.js web框架模块express，-g表示全局安装。

  ```
  $ npm install express -g
  ```

  安装完毕之后在代码中用require()方法引入：

  ```javascript
  var express = require("express")
  ```

- 全局安装与本地安装

  - 全局安装：-g
    - 将安装包放在./user/local目录下或者你的node安装目录下
    - 可以直接在命令行中使用
  - 本地安装：
    - 将安装包放在./node_modules下(运行npm时所在目录)，如果没有这个目录。就在npm执行的目录下生成node_modules目录。
    - 可以通过require()来引入本地安装的包

- 使用package.json

  package.json位于模块目录下，用于定义包的属性。

- 卸载模块，例如卸载express【node.js的web框架模块】

  ```
  $ npm uninstall express
  ```

- 更新模块，例如更新express模块

  ```
  $ npm undate express
  ```

- 搜索模块，例如搜索express模块

  ```
  $ npm search express
  ```

- 创建模块

  - 编写node.js包文件：

    ```javascript
    //保存为myNode.js
    exports.sayHello = function(){
      return "hello world!";
    };
    ```

  - 初始化包描述文件，执行以下命令生成package.json文件：

    ```
    $ npm init -y 
    ```

  - 在npm资源库中注册账号：

    ```
    $ npm adduser
    ```

  - 发布模块

    ```
    $ npm publish
    ```

    