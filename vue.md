1. npm install vue-cli -g  *安装脚手架*  
2. vue init webpack vue_test  *初始化项目*  
3. npm install iview --save  *安装iview*  
   在main.js中
   import iView from 'iview'  
   import 'iview/dist/styles/iview_own.css'  
   Vue.use(iView)  
4. npm install vuex --save    *安装vuex*  
5. npm install axios --save  *安装axios*  
6. 将自定义的css文件，放入**static**目录下，然后在index.html中引入  
<link rel="stylesheet"  href="../static/stylesheet/common.css"></link>  
7. npm run dev  *运行开发服务器*  

