<template>
    <main class="text-white fw-bold py-4">
        {{contentMain}}
    </main>
</template>

<script>
export default {
    name: 'MainMain',
    data() {
        return {
            contentMain: '--> Content goes here <--'
        }
    },
}
</script>

<style lang="scss">
    main {
        background-color: #1c1c1c;
    }
</style>