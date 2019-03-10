# ng7-dynamic-breadcrumb


ng7-dynamic-breadcrumb is a module for [Angular](https://angular.io/) that generates a breadcrumb for any page of your application. It is based on the built-in [Angular router](https://angular.io/docs/ts/latest/guide/router.html).

## [Demo  Example ](https://ng7-dynamic-breadcrumb.stackblitz.io)
## [Demo  Source Example ](https://stackblitz.com/edit/ng7-dynamic-breadcrumb)

# Usage

## Getting started

1.Install `ng7-dynamic-breadcrumb` via npm:

```bash
npm install --save ng7-dynamic-breadcrumb
```

2.Import the `NgDynamicBreadcrumbModule` within your app:

```js
import {NgDynamicBreadcrumbModule} from "ng7-dynamic-breadcrumb";

@NgModule({
  imports: [
    NgDynamicBreadcrumbModule,
  ],
})
```

3.Add a name to your route by adding a `breadcrumb` property in the route's `data`:

```js
const routes: Routes = [
  {
    path: 'page1/:pageOneID',
    component: PageComponent,
    data: {
      title: 'page1',
      breadcrumb: [
        {
          label: 'Page1',
          url: ''
        }
      ]
    },
  },
  {
    path: 'page1/:pageOneID/page2/:pageTwoID',
    component: Page2Component,
    data: {
      title: 'page2',
      breadcrumb: [
        {
          label: 'page1',
          url: '/page1/:pageOneID'
        },
        {
          label: 'page2',
          url: ''
        }
      ]
    },
  },

];
```

4.Put the `NgDynamicBreadcrumbComponent`'s selector within your template:

```html
<app-ng7-dynamic-breadcrumb></app-ng7-dynamic-breadcrumb>
<router-outlet></router-outlet>
```

## Help/Assistance

Developer: Raja Rama Mohan Thavalam <rajaram.tavalam@gmail.com>  


## License


(The MIT License)

Copyright (c) 2019 Raja Rama Mohan T <rajaram.tavalam@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
