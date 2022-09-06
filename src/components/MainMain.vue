<template>
    <section>
        <div class="bg">
            <main class="text-white fw-bold py-4 container">
                <button class="but px-3 py-1">CURRENT SERIES</button>
                <div class="row my-3">
                    <cardForMain class="myCard" v-for="(el, i) in dcComics" :key="i" :dcComics="el" />
                </div>
                <div class="contenitor-but">
                    <button class="but2 px-5 py-2">LOAD MORE</button>
                </div>
            </main>
        </div>
    </section>
</template>

<script>
import dcComics from '@/assets/jsons/dc-comics.json';
import cardForMain from './cardForMain.vue';

export default {
    name: 'MainMain',
    components: {
        cardForMain
    },
    data () {
        return {
            dcComics
        }
    }
}
</script>

<style scoped lang="scss">
section {
    background-image: url('../assets/img/jumbotron.jpg');
    background-repeat: no-repeat;
    background-size: 100% auto;
    background-position: top center;

    padding-top: 390px;

    flex-grow: 1;

    .bg {
        background-color: #1c1c1c;
    }

    main {
        position: relative;
        font-size: 2rem;

        .but,
        .but2 {
            background-color: #0282f9;
            color: #fff;
            border: none;
            transition: background-color 0.2s ease-in-out;

            &:hover{
                background-color: #0055a4;
            }
        }

        .but {
            font-size: 1.5rem;
            font-weight: bold;
            position: absolute;
            top: 0;
            left: 0;
            transform: translateY(-50%);
        }

        .contenitor-but {
            text-align: center;

            .but2 {
                font-size: 0.8rem;
                font-weight: 500;
            }
        }

        .myCard {
            cursor: pointer;
            transition: all 0.1s ease-in-out;
            
            &:hover {
                box-shadow: 0 0 10px #313131;
                transform: scale(1.05);
                border-radius: 5px;
            }
        }
    }
}

@media screen and (max-width: 575.98px) {
    section {
        padding-top: 250px;
    }
}

@media screen and (max-width: 767.98px) {
    section {
        padding-top: 200px;
    }
}
</style>