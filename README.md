# vue-ustmodal

[![Version](https://img.shields.io/npm/v/vue-ustmodal.svg)](https://npmjs.org/package/open-source-npm-package-template)
![Travis (.org)](https://img.shields.io/travis/prokopsimek/open-source-npm-package-template)
[![Downloads/week](https://img.shields.io/npm/dw/vue-ustmodal.svg)](https://npmjs.org/package/open-source-npm-package-template)
[![License](https://img.shields.io/npm/l/vue-ustmodal.svg)](https://github.com/danushka96/vue-ustmodal/blob/master/package.json)
![npm collaborators](https://img.shields.io/npm/collaborators/vue-ustmodal)

## Intro

vue-ustmodal is a modal that can be used in your components without thinking about stylings or modal behaviour.

![](https://i.imgur.com/gEP96qq.gif)


## Getting Started

### Installation

- with NPM
  
  ```$ npm install -save vue-ustmodal``` 
- with Yarn 
  
  ```$ yarn add vue-ustmodal```

### Usage

**Example**

main.js
```javascript=true
import Vue from 'vue'
import App from './App.vue'
import ustModal from "vue-ustmodal";

Vue.config.productionTip = false
Vue.use(ustModal);

new Vue({
  render: h => h(App),
}).$mount('#app')
```
Component.vue
```javascript=true
<template>
<div>
    <div class="modal">
        <button @click="modal = true">Open</button>
        
        <ustModal v-model="modal" :styles="styles"> 
            <h3 slot="title">Custom Header</h3>
            <div slot="body">
                <p>This Modal Body</p>
                <p>This Modal Body</p>
                <p>This Modal Body</p>
                <p>This Modal Body</p>
                <p>This Modal Body</p>
            </div>
            <div slot="actions">
                <button @click="modal=false">Cancel</button>
                <button @click="modal=false">OK</button>
            </div>
        </ustModal>
    </div>
</div>
</template>

<script>
import ustModal from './ustModal'
export default {
    components: {
        ustModal
    },
    data: () =>  ({
        modal: true,
        styles: {
            width: "500px"
        }
    })
}
</script>
```

## Contributing

Feel free to contribute to the Open Source NPM Package Template. If you want to contribute.

## License

The Open Source NPM Package Template is licensed under the [Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

