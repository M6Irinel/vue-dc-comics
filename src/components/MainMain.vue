<template>
    <section>
        <main class="text-white fw-bold py-4 container">
            {{ contentMain }}
        </main>
    </section>
</template>

<script>
export default {
    name: 'MainMain',
    data () {
        return {
            contentMain: '--> Content goes here <--'
        }
    },
}
</script>

<style lang="scss">
section {
    background-color: #1c1c1c;
    flex-grow: 1;

    main {
        font-size: 2rem;
    }
}
</style>