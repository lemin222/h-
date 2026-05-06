<template>
    <div class="container">
        <header>
            <slot name="header">

            </slot>
        </header>
        <main>
            <slot>

            </slot>
        </main>
        <footer>
            <slot name="footer">
            </slot>
        </footer>
    </div>
</template>

<script lang="ts">
export default {
    name: 'Child',
    props: ['url']
}

</script>