<template>
    <div class="col-6 col-md-3 col-lg-2 pt-4">
        <div class="img-card">
            <img class="img-fluid" :src="dcComics.thumb" :alt="dcComics.series" :title="dcComics.type">
        </div>
        <p class="title pt-3">{{dcComics.series}}</p>
    </div>
</template>

<script>
export default {
    props: {
        dcComics: Object
    }
}
</script>

<style scoped lang="scss">
    .img-card{
        aspect-ratio: 1;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top center;
        }
    }

    .title {
        font-size: 0.9rem;
        text-transform: uppercase;
        font-weight: 400;
    }
</style>