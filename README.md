<p align="center">
  <a href="https://bryntum.com/" rel="noopener" target="_blank"><img width="200" src="https://bryntum.com/wp-content/uploads/2022/11/RGB_Bryntum-Logo-Blue-1.svg" alt="Bryntum logo"></a>
</p>

<h1 align="center">Bryntum Grid</h1>

Bryntum Grid is a high performance JavaScript data grid component. It integrates smoothly with React, Vue, Angular, or plain vanilla JS.

For more information about Bryntum Grid, visit the [Bryntum Grid site](https://bryntum.com/products/grid/)

<img src="https://bryntum.com/products/grid/docs/data/Grid/images/getting-started-result.png" alt="Bryntum Grid Screenshot">

## Key Features

* **High Performance** - Handles large datasets with virtual rendering
* **Modern Themes** - Multiple built-in themes with customization support
* **Framework Support** - React, Vue, Angular, and vanilla JavaScript
* **Responsive Design** - Touch-friendly and mobile-optimized
* **TypeScript** - Full TypeScript definitions included
* **Accessible** - WCAG 2.1 compliant with keyboard navigation

## Try Demos

Explore our comprehensive collection of demos:

* [View Online Demos](https://bryntum.com/products/grid/examples/)
* [JavaScript Demos](https://bryntum.com/products/grid/examples/?framework=javascript)
* [React Demos](https://bryntum.com/products/grid/examples/?framework=react)
* [Vue Demos](https://bryntum.com/products/grid/examples/?framework=vue)
* [Angular Demos](https://bryntum.com/products/grid/examples/?framework=angular)

## Bryntum repository access setup

This npm package requires access to the private Bryntum npm repository. You must be logged in as a licensed or trial user to install it.

Please check the [npm repository guide](https://bryntum.com/products/grid/docs/guide/Grid/npm-repository) for detailed information on the sign-up/login process.

## Installation

The installation is performed by issuing the installation command in the root of the application folder. The specific
command depends on the package manager used by the application.

### Core Package

Install using `npm`:

```shell
npm install @bryntum/grid@7.1.1
```

### Framework Wrappers

#### React

```shell
npm install @bryntum/grid-react@7.1.1
```

#### Vue 3

```shell
npm install @bryntum/grid-vue-3@7.1.1
```

#### Angular

```shell
npm install @bryntum/grid-angular@7.1.1
```

## Quick Start

### Vanilla JavaScript

```javascript
import { Grid } from '@bryntum/grid';
import './style.css';

const grid = new Grid({
    appendTo : 'app',
    columns : [
        {
            text   : 'Name',
            field  : 'name',
            flex   : 1,
            editor : {
                type     : 'textfield',
                required : true
            }
        }, {
            text  : 'Age',
            field : 'age',
            width : 100,
            type  : 'number'
        }, {
            text  : 'City',
            field : 'city',
            flex  : 1
        }, {
            text  : 'Food',
            field : 'food',
            flex  : 1
        }, {
            text     : 'Color',
            field    : 'color',
            width    : 80,
            type     : 'color',
            renderer : ({ cellElement, value }) => {
                cellElement.style.color = value;
                cellElement.style.fontWeight = '700';
                return value;
            }
        }
    ],

    data : [
        { id : 1, name : 'Don A Taylor', age : 30, city : 'Moscow', food : 'Salad', color : 'Black' },
        { id : 2, name : 'John B Adams', age : 65, city : 'Paris', food : 'Bolognese', color : 'Orange' },
        { id : 3, name : 'John Doe', age : 40, city : 'London', food : 'Fish and Chips', color : 'Blue' },
        { id : 4, name : 'Maria Garcia', age : 28, city : 'Madrid', food : 'Paella', color : 'Green' },
        { id : 5, name : 'Li Wei', age : 35, city : 'Beijing', food : 'Dumplings', color : 'Yellow' },
        { id : 6, name : 'Sara Johnson', age : 32, city : 'Sydney', food : 'Sushi', color : 'Purple' },
        { id : 7, name : 'Lucas Brown', age : 22, city : 'Toronto', food : 'Poutine', color : 'Orange' },
        { id : 8, name : 'Emma Wilson', age : 27, city : 'Paris', food : 'Croissant', color : 'Pink' },
        { id : 9, name : 'Ivan Petrov', age : 45, city : 'St. Petersburg', food : 'Borscht', color : 'Grey' },
        { id : 10, name : 'Zhang Ming', age : 50, city : 'Shanghai', food : 'Hot Pot', color : 'Purple' },
        { id : 11, name : 'Sophia Martinez', age : 20, city : 'Mexico City', food : 'Tacos', color : 'Crimson' },
        { id : 12, name : 'Noah Smith', age : 55, city : 'Cape Town', food : 'Biltong', color : 'Turquoise' },
        { id : 13, name : 'Isabella Jones', age : 33, city : 'Rio de Janeiro', food : 'Feijoada', color : 'Magenta' },
        { id : 14, name : 'Ethan Taylor', age : 29, city : 'Chicago', food : 'Deep-Dish Pizza', color : 'Cyan' },
        { id : 15, name : 'Olivia Brown', age : 37, city : 'Berlin', food : 'Schnitzel', color : 'Maroon' },
        { id : 16, name : 'Mia Wilson', age : 26, city : 'Rome', food : 'Pasta', color : 'Olive' },
        { id : 17, name : 'Jacob Miller', age : 60, city : 'Amsterdam', food : 'Stroopwafel', color : 'Lime' },
        { id : 18, name : 'Chloe Davis', age : 23, city : 'Los Angeles', food : 'Burger', color : 'Teal' },
        { id : 19, name : 'Aiden Martinez', age : 48, city : 'Buenos Aires', food : 'Asado', color : 'Violet' },
        { id : 20, name : 'Liam Lee', age : 38, city : 'Seoul', food : 'Kimchi', color : 'Indigo' },
        { id : 21, name : 'Sophie Kim', age : 21, city : 'Tokyo', food : 'Ramen', color : 'Pink' },
        { id : 22, name : 'Alexander Nguyen', age : 41, city : 'Hanoi', food : 'Pho', color : 'Coral' },
        { id : 23, name : 'Ella Patel', age : 19, city : 'Mumbai', food : 'Curry', color : 'Amber' },
        { id : 24, name : 'James O Connor', age : 34, city : 'Dublin', food : 'Irish Stew', color : 'Green' },
        { id : 25, name : 'Isabelle Chen', age : 31, city : 'Hong Kong', food : 'Dim Sum', color : 'Brown' }
    ]

});
```

In the `style.css`:

```css
/* FontAwesome is used for icons */
@import "@bryntum/grid/fontawesome/css/fontawesome.css";
@import "@bryntum/grid/fontawesome/css/solid.css";
/* Structural CSS */
@import "@bryntum/grid/grid.css";
/* Bryntum theme of your choice */
@import "@bryntum/grid/svalbard-light.css";
```

Visit our JavaScript [Quick Start guide](https://bryntum.com/products/grid/docs/guide/Grid/quick-start/javascript-npm) to learn more.

## Framework Integrations

Bryntum Grid provides first-class wrappers for popular frameworks:
* React: `@bryntum/grid-react`
* Angular: `@bryntum/grid-angular`
* Vue: `@bryntum/grid-vue`

Each wrapper follows native framework patterns and lifecycle management.

Visit our [Reat](https://bryntum.com/products/grid/docs/guide/Grid/quick-start/react), [Angular](https://bryntum.com/products/grid/docs/guide/Grid/quick-start/angular) 
and [Vue](https://bryntum.com/products/grid/docs/guide/Grid/quick-start/vue-3) Quick Start guides to learn more.

## Themes

Bryntum Grid offers six built-in themes, each available in both light and dark variants:

* Svalbard
* Stockholm
* Visby
* Material 3
* High Contrast
* Fluent 2

| Svalbard Light | Stockholm Dark |
|----------------|----------------|
| ![Svalbard Light](https://bryntum.com/products/grid/docs/data/Grid/images/themes/thumb.svalbard-light.png) | ![Stockholm Dark](https://bryntum.com/products/grid/docs/data/Grid/images/themes/thumb.stockholm-dark.png) |
| **Svalbard Light** | **Stockholm Dark** |

| Visby Light | Material 3 Dark |
|------------|----------------|
| ![Visby Light](https://bryntum.com/products/grid/docs/data/Grid/images/themes/thumb.visby-light.png) | ![Material 3 Dark](https://bryntum.com/products/grid/docs/data/Grid/images/themes/thumb.material3-dark.png) |
| **Visby Light** | **Material 3 Dark** |

| High Contrast Light | Fluent 2 Dark |
|--------------------|----------------|
| ![High Contrast Light](https://bryntum.com/products/grid/docs/data/Grid/images/themes/thumb.high-contrast-light.png) | ![Fluent 2 Dark](https://bryntum.com/products/grid/docs/data/Grid/images/themes/thumb.fluent2-dark.png) |
| **High Contrast Light** | **Fluent 2 Dark** |

Learn more about [theming and customization](https://bryntum.com/products/grid/docs/guide/Grid/customization/styling).

## Online references

* [Bryntum npm repository guide](https://bryntum.com/products/grid/docs/guide/Grid/npm-repository)
* [Bryntum Grid documentation](https://bryntum.com/products/grid/docs/)
* [Bryntum Grid examples](https://bryntum.com/products/grid/examples/)
* [Bryntum Support Forum](https://forum.bryntum.com/)
* [Contact us](https://bryntum.com/contact/)

## License and copyright

Bryntum Grid is commercial software and requires a paid license. Please visit the 
[Bryntum Grid End User License](https://bryntum.com/products/grid/license/) for the full text of the license.

Copyright © 2009-2026, Bryntum
All rights reserved.

