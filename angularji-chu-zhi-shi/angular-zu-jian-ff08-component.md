# Angular 组件（component）

![](/assets/component.png)

```js
import { Component } from '@angular/core';

//组件源数据装饰器
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'app';
}
```





