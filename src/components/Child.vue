<template>
    <a :href="url"> 
        <slot></slot>
    </a>
</template>

<script lang="ts">
export default {
    name: 'Child',
    props: ['url']
}

</script>