# icart9
# start git
## create new branch feature #1
# start new angular project 
```
ng new ng-icart9
```
```
cd ng-icart9
```
```
ng serve --open
```
### notice start page

## add parts, navbar 
```
ng g c top-bar
```
## update app/top-bar/top-bar.component.html
## update app/styles.css
## update index.html

# feature#2 add product list page
```
ng g c product-list
```
## update routing app/app.routing.module.ts
```
import { ProductListComponent } from './product-list/product-list.component';

const routes: Routes = [
  { path: '', component: ProductListComponent },
];
```
notice product works load on top-level
## create new file app/product.ts
add json

