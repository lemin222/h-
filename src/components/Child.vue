<template>
    <a :href="url"> baidu</a>
</template>

<script lang="ts">
export default {
    name: 'Child',
    props: ['url']
    /*在这段代码中，:href="url" 和 props: ['url'] 的作用如下：
1. props: ['url']
props 是 Vue 组件中用来接收父组件传递数据的属性。
这里定义了一个名为 url 的 prop，表示这个组件可以从父组件接收一个名为 url 的值。
父组件在使用 <Child> 组件时，可以通过绑定 url 属性来传递数据，例如：
2. :href="url"
:href 是 Vue 的绑定语法，等价于 v-bind:href，表示将 url 的值动态绑定到 <a> 标签的 href 属性上。
这里的 url 是从 props 中接收到的值。
例如，如果父组件传递的 url 是 "https://www.baidu.com"，那么最终渲染的 HTML 会是：
总结
props: ['url'] 定义了组件可以接收一个名为 url 的数据。
:href="url" 将接收到的 url 数据动态绑定到 <a> 标签的 href 属性上，从而实现动态链接。
3.如果父组件要传递多个属性，可以在 props 中定义多个属性，例如：
  数组形式
export default {
    name: 'Child',
    props: ['url', 'text'] // 接收多个属性
}
   对象形式 
   props: {
        url: {
            type: String, // 指定类型
            required: true // 必须传递
        },
        text: {
            type: String,
            default: 'Default Text' // 设置默认值
        }
    }
*
}

</script>