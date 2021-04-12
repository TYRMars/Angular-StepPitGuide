# Angular 模块（module）

```javascript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';

import { AppComponent } from './app.component';

@NgModule({
  declarations: [
    AppComponent  // 组件声明引入、管道声明引入
  ],
  imports: [
    BrowserModule // 引入相关处理模块
  ],
  providers: [], //服务
  bootstrap: [AppComponent] //声明主组件
})
export class AppModule { }
```

