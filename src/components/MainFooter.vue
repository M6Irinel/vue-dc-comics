<template>
    <footer>
        <TopFooter />

        <div class="centerFooter container">
            <div class="list" v-for="(list, i) in footerList" :key="i">
                <div v-for="(list2, i2) in list" :key="i2">
                    <h3> {{list2.title}} </h3>
                    <ul>
                        <li v-for="(list3, i3) in list2.list" :key="i3">
                            <a :href="list3.href"> {{list3.content}} </a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="ms-auto">
                <img class="logo-footer" src="@/assets/img/dc-logo-bg.png" alt="dc logo bg">
            </div>
        </div>

        <div class="bottom">
            <div class="container">
                <div>
                    <button>SIGN-UP NOW!</button>
                </div>

                <div class="right">
                    <a href="#">FOLLOW US</a>
                    <a :href="el.href" v-for="(el, i) in footerBottom" :key="i">
                        <img :src="el.src" alt="el.alt" :title="el.alt">
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import TopFooter from '@/components/TopFooter.vue';
import footerList from '@/assets/jsons/footer-list.json';

const footerBottom = [
    {
        href: '#',
        src: require( '../assets/img/footer-facebook.png' ),
        alt: 'facebook'
    },
    {
        href: '#',
        src: require( '../assets/img/footer-twitter.png' ),
        alt: 'twitter'
    },
    {
        href: '#',
        src: require( '../assets/img/footer-youtube.png' ),
        alt: 'youtube'
    },
    {
        href: '#',
        src: require( '../assets/img/footer-pinterest.png' ),
        alt: 'pinterest'
    },
    {
        href: '#',
        src: require( '../assets/img/footer-periscope.png' ),
        alt: 'periscope'
    },
];

export default {
    name: 'MainFooter',
    data () {
        return {
            footerList,
            footerBottom
        }
    },
    components: {
        TopFooter
    }
}
</script>

<style lang="scss">
footer {
    background-image: url('../assets/img/footer-bg.jpg');
    background-position: center;
    background-size: cover;

    .centerFooter {
        // padding: 50px 0;
        display: flex;
        gap: 30px;
        position: relative;
        // overflow: hidden;

        .list {
            position: relative;
            z-index: 1000;
            padding: 40px 0;
        }

        .logo-footer {
            height: 150%;
            transform: translateY(-17%);

            position: absolute;
            // top: -120px;
            right: 0;
            // width: 650px;
        }

        h3 {
            color: #fff;
            font-size: 1.2rem;
            font-weight: bold;
            padding-bottom: 0.6rem;
        }

        ul {
            list-style: none;
            padding: 0;

            li a {
                color: #838383;
                text-decoration: none;
                list-style: none;
                font-size: 0.8rem;
                transition: color 0.1s ease-in-out;

                &:hover {
                    color: #fff;
                }
            }
        }

        @media screen and (max-width: 767.98px) {
            .logo-footer {
                width: 100%;
                height: auto;
                transform: translateY(-17%);
            }
        }
    }

    .bottom {
        position: relative;
        background-color: #303030;
        z-index: 1000;
        padding: 35px;

        .container {
            padding: 0;
            display: flex;
            align-items: center;
        }

        button {
            border: 2px solid #008aff;
            background-color: transparent;
            color: #fff;
            font-weight: bold;
            padding: 10px;
            transition: color 0.1s ease-in-out;

            &:hover {
                color: #c6c6c6;
            }
        }

        & > div {
            display: flex;
            justify-content: space-between;

            .right {
                display: flex;
                gap: 20px;
                
                a:first-of-type {
                    text-decoration: none;
                    font-weight: bold;
                    font-size: 1.2rem;
                    transition: all 0.1s ease-in-out;

                    &:hover {
                        color: #008aff;
                    }
                }

                a:not(:first-of-type):hover {
                    filter: brightness(2);
                }
            }
        }
    }
}
</style>