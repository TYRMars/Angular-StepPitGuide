# Angular 依赖注入（Dependency Injection）

### 依赖注入

* 依赖注入：Dependency Injection 简称DI
  * 目的是如何实现控制反转，
* 控制反转：Inversion of Control 简称IOC
  * 目的是将依赖控制权从代码内部转移到代码外部

```js
var product = new Prodcut();
createShipment(product);
```

```

```

### 使用依赖注入的好处

* 例：当一个商品，想被重复使用

```js
@NgModule({
    providers:[ProductService]
    // providers: []
})
export class AppModule {}

@Compnent({
   //···
})

export class ProductComponnet {
    product: Product;
    constructor(productService: ProductService) {
        this.product = productService.getProduct();
    }
}
```

### 注入器与提供器

* 注入器

```js
constructor(private productService: ProductService) {···}
```

* 提供器

```js
//provide:ProductService 生成token
providers:[ProductService]
providers:[{provide:ProductService,useClass:ProductService}] //useClass 使用 new
```



