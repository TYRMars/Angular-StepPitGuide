# Angular 路由（Route）

### 路由基本知识

| 名称 | 简介 |
| :---: | :---: |
| Routes | 路由配置，保存着哪个URL对应展示哪个组件，以及在哪个    RouterOutlet中展示组件 |
| RoutOutlet | 在html中标记路由内容呈现位置的占位符指令 |
| Router | 负责运行时执行路由的对象，可以通过调用其navigate\(\)和     navgateByUrl\(\)方法来导航到一个指定的路由 |
| RouterLink | 在HTML中声明路由导航的指令 |
| ActivatedRoute | 当前激活的路由对象，保存着当前路由的信息，如路由地址，路由参数等。 |

### 路由传递参数

##### 查询参数中传递数据

* 类似`/product?id=1&name=2` =&gt; `ActivatedRoute.queryParams[id]` 这种方式
  * 目标组件中获取采用`ActivedRoute.queryParams[id]` 

##### 路由路径中传递参数

* 类似`{path:/product/:id} `=&gt;` /product/1` =&gt;`ActivatedRoute.queryParams[id]`  

##### 路由配置中传递数据

* 类似`{path:/product， component: ProductComponent, data:[{isProd:true}]} `=&gt;`ActivatedRoute.data[0]['isProd']`  



