# diagram-vue
A vue component library of diagrams  
[Demo](https://diagram.netlify.com/)

## Installaion
```sh
npm i install --save
```

## Usage
### Template
```html
<Diagram
    :width="2000"
    :height="1000"
    :nodes="nodes"
    :links="links"
    linkColor="#ffeaa7"
    :editable="editable"
    :labels="{
        edit: 'Edit',
        remove: 'Remove',
        link: 'Link',
        select: 'Select'
    }"
    @editNode="editNode"
    @nodeChanged="nodeChanged"
    @linkChanged="linkChanged"
    >
</Diagram>
```
### Import
```js
import Diagram from 'diagram-vue'
```
### Props
```js
props: {
    width: Number,
    height: Number,
    nodes: Array,
    links: Array,
    editable: Boolean,
    linkColor: String,
    labels: Object
}
```
[Sample data](https://github.com/pb10001/diagram-vue/blob/master/src/data.js) helps you know the data structure of nodes and links.
### Events
```js
editNode(node /* selected node */) {
    /* event handler */
},
nodeChanged(nodes /* array of nodes */) {
    /* event handler */
},
linkChanged(links /* array of links */) {
    /* event handler */
}

```
## Development

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn run serve
```

### Compiles and minifies for production
```
yarn run build
```

### Run your tests
```
yarn run test
```

### Lints and fixes files
```
yarn run lint
```

### Run your end-to-end tests
```
yarn run test:e2e
```

### Run your unit tests
```
yarn run test:unit
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
