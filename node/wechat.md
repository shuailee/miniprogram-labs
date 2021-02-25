#### 目录结构

![](F:\my-project\wx\img\image-20210225111820420.png)

（1）**根目录**

- **app.js(必须，小程序的主流程代码)  App({   ...  })**
  - onLaunch 函数，初始化时调用
  - onShow 函数，程序显示时调用
  - onHide 函数，程序隐藏时调用
  - onError 函数，发生错误时调用
  - 其他 任意值，可以在整个项目中访问
- **app.json(必须，小程序的全局配置)**
  - pages，页面路径，每增加一个路径对应pages文件夹就会生成四个页面文件
  - window，窗口的默认样式
  - tabBar，窗口底部的tab的样式
  - networkTimeout，网络超时时间
  - debug，是否开启debug模式
- app.wxss(可选，全局样式)
- project.config.json(可选，开发者工具配置)
  - 此文件用于定义开发者工具的个性化定制，比如界面颜色，编译配置等等，让项目设置再切换开发主机时依然保留
  - https://developers.weixin.qq.com/miniprogram/dev/devtools/projectconfig.html

（2）**pages（页面）**

一个小程序页面由四个文件组成，分别是：

| 文件类型                                                     | 必需 | 作用                                                         |
| :----------------------------------------------------------- | :--- | :----------------------------------------------------------- |
| [js](https://developers.weixin.qq.com/miniprogram/dev/framework/app-service/page.html) | 是   | 页面逻辑                                                     |
| [wxml](https://developers.weixin.qq.com/miniprogram/dev/framework/view/wxml/) | 是   | 页面结构,类似网页开发的html文件，语法：https://developers.weixin.qq.com/miniprogram/dev/framework/view/wxml/ |
| [json](https://developers.weixin.qq.com/miniprogram/dev/framework/config.html#页面配置) | 否   | 页面静态数据配置文件                                         |
| [wxss](https://developers.weixin.qq.com/miniprogram/dev/framework/view/wxss.html) | 否   | 页面样式表                                                   |

**注意：为了方便开发者减少配置项，描述页面的四个文件必须具有相同的路径与文件名，他们是根据全局app.json文件里的pages配置动态生成的，例如：**

- index
  - **index.wxml(必须)**
  - **index.js(必须)**
  - index.json(可选)
  - index.wxss(可选)

二 注意点

- json文件都是被包裹在{}中，并以key-value方式展示。注意，key一定要加上双引号，没加双引号，或者加了单引号都会报错
- json的值只能是数字，字符串(需要加双引号)，布尔值，数组(放在[]中)，对象(放在{}中)，或者null，不支持undefined以及其它数据结构



三 WXSS 和 WXML

   s

https://www.cnblogs.com/echolun/p/12709761.html

#### WXSS

| 项目            | 例子         | 含义                        |
| --------------- | ------------ | --------------------------- |
| #id             | #parent      | 选择id='parent'的组件       |
| .class          | .child       | 选择所有class='child'的组件 |
| element         | view         | 选择所有view组件            |
| element,element | view,text    | 选择所有view组件和text组件  |
| ::after         | text::after  | 在text组件后面插入内容      |
| ::before        | text::before | 在text组件前面插入内容      |

rpx（responsive pixel）: 可以根据屏幕宽度进行自适应











https://www.cnblogs.com/echolun/p/12741159.html

[https://developers.weixin.qq.com/miniprogram/dev/framework/config.html#%E5%85%A8%E5%B1%80%E9%85%8D%E7%BD%AE](https://developers.weixin.qq.com/miniprogram/dev/framework/config.html#全局配置)





