1. `npm install vue-cli -g`  *安装脚手架*  
2. `vue init webpack vue_test`  *初始化项目, install vue-router选择yes*  
3. `npm install iview --save`  *安装iview*  
   在main.js中
   `import iView from 'iview'    
   import 'iview/dist/styles/iview_own.css'    
   Vue.use(iView)`    
4. `npm install vue-cookie --save`     *安装cookie*    
   import VueCookies from 'vue-cookies'    
   Vue.use(VueCookies)    
4. ~~`npm install --save-dev webpack@latest webpack-cli`    *安装webpack以及webpack-cli* 使用3而不是4          
5. `npm i element-ui -S`         *安装element ui*      
   按需应用需要安装一下package          
   `npm install babel-plugin-component -D`    
   修改.babelrc(查elementui文档)    
   import Vue from 'vue';          
   `import { Button, Select } from 'element-ui';`             
   import App from './App.vue';           
   
   `Vue.use(Button)`            
4. `npm install vuex --save`    *安装vuex*  
   新建文件mainState.js，在其中定义state/mutations/getter/actions  
   在main.js中执行  
   `import mainState from './vuex/mainState'`  引入配置  
   `import Vuex from 'vuex'`                   引入vuex  
   `Vue.use(Vuex)`                             将vuex作为vue的中间件   
   `var store=new Vuex.Store({`                //通过模块的方法载入vuex的配置  
   `  modules:{  
       mainState  
     }  
   }) `  
5. `npm install axios --save`  *安装axios*  
6. 将自定义的css文件，放入**static**目录下，然后在index.html中引入  
`<link rel="stylesheet"  href="../static/stylesheet/common.css"></link>`  
7. 修改config/index.js，添加一个函数，用来自动生成测试路由  
`function generateProxyTable({baseUrl}){    
  let result={}          
  let target='http://127.0.0.1:3000' //发出的请求路由到那个路径            
  let changeOrigin=true   //修改原始url           
  for(let singleEle of baseUrl){            
    result[singleEle]={          
      target:target,           
      changeOrigin:changeOrigin,         
      pathRewrite:{          
        [`^${singleEle}`]:`${singleEle}`            
      }            
    }           
  }              
  return result          
}`   
8. 安装grunt和相关包，转换less到css  
`npm install -g  grunt-cli`  
      `npm install --save-dev grunt`  
      `npm install --save-dev grunt-postcss grunt-contrib-less grunt-contrib-watch grunt-contrib-csslint`  
9. `npm run dev`  *运行开发服务器*  

