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
    }
  }
}

</script>
<template>
  <Child url="http://www.bing.com">
    <button color="blue">youdao</button>

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
