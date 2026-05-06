<script lang="ts">

import Child from './components/Child.vue'
export default {
  name: 'App',
  components: {
    Child
  },
  data() {
    return {
      user: {
        name: '哈默'
      }
      /*
      v-slot="slotProps" 的作用是接收子组件插槽中传递的作用域数据，也就是作用域插槽的功能。

详细解释
1. 什么是作用域插槽？
作用域插槽（Scoped Slot）是 Vue 中的一种插槽类型，允许子组件向父组件传递数据。父组件可以通过 v-slot 指令接收这些数据，并在插槽内容中使用。

在你的代码中，Child 组件的插槽定义如下：

这里，子组件通过 slot 标签向插槽传递了一个名为 slotProperty 的数据，其值是 url（即子组件的 props）。

2. 父组件如何接收数据？
在父组件中，使用 v-slot="slotProps" 来接收子组件传递的数据：

v-slot="slotProps"：表示接收子组件通过插槽传递的数据，并将其存储在 slotProps 对象中。
slotProps.slotProperty：通过 slotProps 对象访问子组件传递的 slotProperty 数据。
在这个例子中，slotProperty 的值是 url，即 "http://www.bing.com"。

最终渲染的内容是：

3. 总结
子组件通过 <slot :slotProperty="url"> 向插槽传递数据。
父组件通过 v-slot="slotProps" 接收这些数据。
父组件可以通过 slotProps.slotProperty 使用子组件传递的数据。
      */
    }
  }
}

</script>
<template>
  <Child url="http://www.bing.com" v-slot="slotProps">
    连接地址为{{ slotProps.slotProperty }}
  </Child>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
