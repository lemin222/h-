<template>
    <a :href="url">
        <slot :slotProperty="url"></slot>
    </a>
</template>

<script lang="ts">
export default {
    name: 'Child',
    props: ['url']
}

</script>