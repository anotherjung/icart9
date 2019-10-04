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

## update product-list page to display data from products.ts, and add share button
### product-list.component.html
```
<h2>Products</h2>

<div *ngFor="let product of products">

    <h3>
      <a [title]="product.name + ' details'">
        {{ product.name }}
      </a>
    </h3>
  
    <p *ngIf="product.description">
      Description: {{ product.description }}
    </p>

        <button (click)="share()">
            Share
        </button>
  
  </div>
  ```

## create new file app/products.ts
add json

## update product-list.components.ts
```
import { products } from '../products';

export class ProductListComponent implements OnInit {
  products = products;

  share() {
    window.alert('The product has been shared!');
  }
```

