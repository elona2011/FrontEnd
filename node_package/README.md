国内源，同官源，适合国内用：
npm config set registry http://registry.cnpmjs.org
官方源：
npm config set registry "http://registry.npmjs.org/"


如果卡顿，可尝试关闭https
npm config set strict-ssl false


cnpm用法：
1.安装cnpm工具
npm install -g cnpm --registry=http://r.cnpmjs.org
或npm install -g cnpm --registry=http://registry.npm.taobao.org
2.使用cnpm安装模块
cnpm install xxx
原文：http://segmentfault.com/a/1190000000471219

npm install microtime --registry=http://r.cnpmjs.org --disturl=http://dist.cnpmjs.org


grunt-cli会执行当前目录中package.json文件指定的grunt版本，来读取当前目录下的gruntfile的配置文件，然后按其中的配置项来执行自动化。
之所以这样是为了多个grunt版本并存，来支持新老项目。