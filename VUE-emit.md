# What is _Emit_ in Vue

> Emit is a custom event in vue.
>
> > Custom event is a way to communicate from child component to parent component.  
> > with Custom event parent Components can listen child Components Events.
>
> _There is anotehr way of communication between parent and child component.  
> and that is `props` . the difference between these two is_
>
> - _**with `props` data from parent component can be passed to the child component.**_
>
> - _**with `emit` parent component can listen child components Events. (data from child component can be passed to the parent component) .**_

## [Example 1](VUE-emit.md)

## This is a **_Root Component (Parent/ App Component)_**

```Vue
<template>
  <h2>
    <span class="log-in" @click="getBlock">Click here</span> to get the box
  </h2>
  <block v-show="showBlock" @close="showBlock = false" />
</template>

<script>
import Block from './components/Block.vue';
export default {
  name: 'App',
  components: { Block },

  data() {
    return {
      showBlock: false,
    };
  },

  methods: {
    getBlock() {
      this.showBlock = true;
    },
  },
};
</script>
```

## and This is a **_Child Component_**

```Vue
<template>
  <div class="container">
    <div class="box" @click="$emit('close')">
      <p>click</p>
    </div>
  </div>
</template>
```

The `'close'` **_Custom Event_** is changing `showBlock` data, that is in the **_Parent Component_**
