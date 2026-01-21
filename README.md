<p align="center">
  <a href="https://bryntum.com/" rel="noopener" target="_blank"><img width="350" src="https://bryntum.com/wp-content/uploads/2022/11/RGB_Bryntum-Logo-Blue-1.svg" alt="Bryntum logo"></a>
</p>

# Bryntum Gantt

Bryntum Gantt is a full featured Gantt chart for project management with support for a big amount of features. It integrates smoothly with React, Vue, Angular, or plain vanilla JS.

For more information about Bryntum Gantt, visit the [Bryntum Gantt site](https://bryntum.com/products/gantt/).

<img src="https://bryntum.com/products/gantt/docs/data/Gantt/images/getting-started-result.png" alt="Bryntum Gantt Screenshot">

## Key Features

* **High Performance** - Handles large datasets with virtual rendering
* **Modern Themes** - Multiple built-in themes with customization support
* **Framework Support** - React, Vue, Angular, and vanilla JavaScript
* **Responsive Design** - Touch-friendly and mobile-optimized
* **TypeScript** - Full TypeScript definitions included
* **Accessible** - WCAG 2.1 compliant with keyboard navigation

## Try Demos

Explore our comprehensive collection of demos:

* [View Online Demos](https://bryntum.com/products/gantt/examples/)
* [JavaScript Demos](https://bryntum.com/products/gantt/examples/?framework=javascript)
* [React Demos](https://bryntum.com/products/gantt/examples/?framework=react)
* [Vue Demos](https://bryntum.com/products/gantt/examples/?framework=vue)
* [Angular Demos](https://bryntum.com/products/gantt/examples/?framework=angular)

## Bryntum repository access setup

This npm package requires access to the private Bryntum npm repository. You must be logged in as a licensed or trial user to install it.

Please check the [npm repository guide](https://bryntum.com/products/gantt/docs/guide/Gantt/npm-repository) for detailed information on the sign-up/login process.

## Installation

The installation is performed by issuing the installation command in the root of the application folder. The specific
command depends on the package manager used by the application.

### Core Package

Install using `npm`:

```shell
npm install @bryntum/gantt@7.1.1
```

### Framework Wrappers

#### React

```shell
npm install @bryntum/gantt-react@7.1.1
```

#### Vue 3

```shell
npm install @bryntum/gantt-vue-3@7.1.1
```

#### Angular

```shell
npm install @bryntum/gantt-angular@7.1.1
```

## Quick Start

### Vanilla JavaScript

```javascript
import { Gantt } from '@bryntum/gantt';
import './style.css';

const gantt = new Gantt({
    appendTo  : 'app',
    startDate : new Date(2022, 0, 1),
    endDate   : new Date(2022, 0, 10),
    columns   : [
        { type : 'name', width : 160 }
    ],
    project : {

        // Automatically introduces a `startnoearlier` constraint for tasks that (a) have no predecessors,
        // (b) do not use constraints and (c) aren't `manuallyScheduled`
        autoSetConstraints : true,
        tasks              : [
            {
                id       : 1,
                name     : 'Documentation Project',
                expanded : true,
                children : [
                    {
                        id       : 2,
                        name     : 'Preparation',
                        expanded : true,
                        children : [
                            { id : 6, name : 'Proof-read docs', startDate : '2026-01-02', endDate : '2026-01-09' },
                            { id : 3, name : 'Release docs', startDate : '2026-01-09', endDate : '2026-01-10' }
                        ]
                    },
                    {
                        id       : 4,
                        name     : 'Development',
                        expanded : true,
                        children : [
                            { id : 7, name : 'Write API docs', startDate : '2026-01-05', endDate : '2026-01-12' },
                            { id : 8, name : 'Write tutorials', startDate : '2026-01-10', endDate : '2026-01-16' },
                            { id : 9, name : 'Create examples', startDate : '2026-01-12', endDate : '2026-01-18' }
                        ]
                    },
                    {
                        id       : 5,
                        name     : 'Review & Release',
                        expanded : true,
                        children : [
                            { id : 10, name : 'Team review', startDate : '2026-01-18', endDate : '2026-01-20' },
                            { id : 11, name : 'Final approval', startDate : '2026-01-20', endDate : '2026-01-21' },
                            { id : 12, name : 'Public release', startDate : '2026-01-22', endDate : '2026-01-22' }
                        ]
                    }
                ]
            }
        ],
        dependencies : [
            { fromTask : 6, toTask : 3 },
            { fromTask : 7, toTask : 8 },
            { fromTask : 8, toTask : 9 },
            { fromTask : 9, toTask : 10 },
            { fromTask : 10, toTask : 11 },
            { fromTask : 11, toTask : 12 }
        ]
    }
});
```

In the `style.css`:

```css
/* FontAwesome is used for icons */
@import "@bryntum/gantt/fontawesome/css/fontawesome.css";
@import "@bryntum/gantt/fontawesome/css/solid.css";
/* Structural CSS */
@import "@bryntum/gantt/gantt.css";
/* Bryntum theme of your choice */
@import "@bryntum/gantt/svalbard-light.css";
```

Visit our JavaScript [Quick Start guide](https://bryntum.com/products/gantt/docs/guide/Gantt/quick-start/javascript-npm) to learn more.

## Framework Integrations

Bryntum Grid provides first-class wrappers for popular frameworks:
* React: `@bryntum/grid-react`
* Angular: `@bryntum/grid-angular`
* Vue: `@bryntum/grid-vue`

Each wrapper follows native framework patterns and lifecycle management.

Visit our [Reat](https://bryntum.com/products/gantt/docs/guide/Gantt/quick-start/react), [Angular](https://bryntum.com/products/gantt/docs/guide/Gantt/quick-start/angular) 
and [Vue](https://bryntum.com/products/gantt/docs/guide/Gantt/quick-start/vue-3) Quick Start guides to learn more.

## Themes

Bryntum Gantt offers six built-in themes, each available in both light and dark variants:

* Svalbard
* Stockholm
* Visby
* Material 3
* High Contrast
* Fluent 2

| Svalbard Light | Stockholm Dark |
|----------------|----------------|
| ![Svalbard Light](https://bryntum.com/products/gantt/docs/data/Gantt/images/themes/thumb.svalbard-light.png) | ![Stockholm Dark](https://bryntum.com/products/gantt/docs/data/Gantt/images/themes/thumb.stockholm-dark.png) |

| Visby Light | Material 3 Dark |
|------------|----------------|
| ![Visby Light](https://bryntum.com/products/gantt/docs/data/Gantt/images/themes/thumb.visby-light.png) | ![Material 3 Dark](https://bryntum.com/products/gantt/docs/data/Gantt/images/themes/thumb.material3-dark.png) |

| High Contrast Light | Fluent 2 Dark |
|--------------------|----------------|
| ![High Contrast Light](https://bryntum.com/products/gantt/docs/data/Gantt/images/themes/thumb.high-contrast-light.png) | ![Fluent 2 Dark](https://bryntum.com/products/gantt/docs/data/Gantt/images/themes/thumb.fluent2-dark.png) |

Learn more about [theming and customization](https://bryntum.com/products/gantt/docs/guide/Gantt/customization/styling).

## Online references

* [Bryntum npm repository guide](https://bryntum.com/products/gantt/docs/guide/Gantt/npm-repository)
* [Bryntum Gantt documentation](https://bryntum.com/products/gantt/docs/)
* [Bryntum Gantt examples](https://bryntum.com/products/gantt/examples/)
* [Bryntum Support Forum](https://forum.bryntum.com/)
* [Contact us](https://bryntum.com/contact/)

## License and copyright

Bryntum Gantt is commercial software and requires a paid license. Please visit the 
[Bryntum Gantt End User License](https://bryntum.com/products/gantt/license/) for the full text of the license.

Copyright © 2009-2026, Bryntum
All rights reserved.

