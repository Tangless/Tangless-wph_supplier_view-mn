#wph_client_m_view

##项目本地启动步骤：

### host配置
将以下域名地址指向本机(127.0.0.1)：
m.wph.com
view.wph.com
global.wph.com
sm.wph.com
sview.wph.com
sglobal.wph.com
www.wph.com
app.wph.com
sapp.wph.com

### 移动端项目工程运行（m/sm）
1，在根目录下运行 npm i ；
2，在/src/node_modules/nodejs/ 目录下运行 npm i ；
3，将/src/node_modules/nodejs/ 目录下的 /@po-to 和 /@type 两个文件夹拷贝到 /src/node_modules/nodejs/node_modules/ 目录下；
4，运行 gulp； 
5，本地服务访问地址： m.wph.com:8888   sm.wph.com:9999

ps: 如果安装了npm淘宝镜像cnpm，最好在执行步骤2的时候不要选择cnpm；因为cnpm的包索引方式会导致gulp运行失败，具体原因，我也不知道。。。。




##工程结构目录说明

###前端JS框架：
src/views/node_modules/@po-to/tomato
src/views/node_modules/@po-to/tomato-jquery

###客户端基本文件：
1，src\node_modules\views\global\common\API 前端ajax请求api的总文件
2，src\node_modules\views\global\common\Funs 前端函数库
3，src\node_modules\views\global\common\Model 前端的全局数据
4，src\node_modules\views\global\common\Project 模块的基类
5，src\node_modules\views\global\common\config-js.idx 合并总的JS

###nodejs目录文件：
1，src\node_modules\nodejs\global\api        node请求api总文件   //已废弃
2，src\node_modules\nodejs\global\model      node端数据模型  （主要用于typescript的静态类型检查，保证数据格式统一） 
3，src\node_modules\nodejs\m                 控制器目录，每一个页面或者模块，都对应有一个控制器，控制器负责组装页面模版和数据并渲染返回
8，src\node_modules\nodejs\index.ts          以前node端入口文件，现在作为本地静态服务的配置文件


###服务器发布：

#### 88ba (线上测试服务器)
客户手机版：/var/www/dev/wph_view 
编译执行文件： git.py
编译执行命令： python git.py

工程商手机版： /var/www/dev/wph_supplier_view
编译执行文件： git.py
编译执行命令： python git.py

客户pc版: /var/www/dev/wph_client_view_www
编译执行文件： git.py
编译执行命令： python git.py

#### wanpinghui （线上正式环境）
客户手机版：/var/www/dev/wph_view 
编译执行文件： git.py
编译执行命令： python git.py

工程商手机版： /var/www/dev/wph_supplier_view
编译执行文件： git.py
编译执行命令： python git.py

客户pc版: /var/www/dev/wph_client_view_www
编译执行文件： git.py
编译执行命令： python git.py
