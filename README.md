# handerbars
## 手机一定要预编译，不管文件是否复杂
>* 如何预编译Handlebars模板，众所周知，如果在运行时去编译一些东西是非常影响性能的，Handlebars同样如此，如果每次都在加载页面的时候，在js中通过Handlebar.compile(template_source)的话，如果模板简单就不说了，如果模板非常复杂，夸张点说，让客户端的浏览器未响应也不是不可能。
>*handerbars.js 在pc上的兼容性还是很好的，直接引入handerbars.js就可以用，但是对于客户端h5,webview一定要换方案，不然对于米渣这种手机，会出现webview崩掉，页面出现吐代码的情况，这就是手机硬件设施，各种不达标导致的，为了解决客户端app中也能够正常渲染模板，需要用到handerbar预编译
>* 要实现Handlebars的预编译非常简单，只需要通过npm 安装他的npm包就可以了 npm install -g handlebars
>* 这时候，handlebars的模板也不用再像入门教程中写的那样通过script标签嵌在Html的页面中了，我们需要把对应的模板写在对应的模板文件里面，handlebars的模板文件就是以.handlebars扩展名结尾的文件。比如有如下文件

##sample.handlebars
```
npm install -g handlebars 
//在crm上输入以下命令
handlebars sample.handlebars -m -f  sample.hbs.js(这个名字是可以随便写的但是后缀都不能变)
Handlebars.templates.sample(context, options);
handlebars.runtime.js替换handlebars.js
```
