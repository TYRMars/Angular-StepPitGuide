# Angular 依赖注入（DI）

## 依赖注入

* 依赖注入：Dependency Injection 简称DI
  * 目的是如何实现控制反转，
* 控制反转：Inversion of Control 简称IOC
  * 目的是将依赖控制权从代码内部转移到代码外部

```javascript
var product = new Prodcut();
createShipment(product);
```

```text

```

## 使用依赖注入的好处

* 例：当一个商品，想被重复使用

```javascript
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

## 注入器与提供器

* 注入器

```javascript
constructor(private productService: ProductService) {···}
```

* 提供器

```javascript
//provide:ProductService 生成token
providers:[ProductService]
providers:[{provide:ProductService,useClass:ProductService}] //useClass 使用 new
// 提供器是通过token，来匹配注入器
providers:[{provide:ProductService,useClass:AnotherProductService}]
// 使用工厂模式初始化
providers:[{provide:ProductServuce,useFactory:()=> {···}}]
```

