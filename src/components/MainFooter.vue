<template>
    <footer>
        <TopFooter />

        <div class="centerFooter container">
            <div class="list">
                <div>
                    <h3>DC COMICS</h3>
                    <ul>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>
                </div>
                <div>
                    <h3>SHOP</h3>
                    <ul>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a></li>
                    </ul>
                </div>
            </div>
            <div class="list">
                <div>
                    <h3>DC</h3>
                    <ul>
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Privacy policy (New)</a></li>
                        <li><a href="#">Ad Choices</a></li>
                        <li><a href="#">Advartising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptions</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Certificates</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                </div>
            </div>
            <div class="list">
                <div>
                    <h3>SITES</h3>
                    <ul>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
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
                    <a href="#">
                        <img src="@/assets/img/footer-facebook.png" alt="facebook">
                    </a>
                    <a href="#">
                        <img src="@/assets/img/footer-twitter.png" alt="twitter">
                    </a>
                    <a href="#">
                        <img src="@/assets/img/footer-youtube.png" alt="youtube">
                    </a>
                    <a href="#">
                        <img src="@/assets/img/footer-pinterest.png" alt="pinterest">
                    </a>
                    <a href="#">
                        <img src="@/assets/img/footer-periscope.png" alt="periscope">
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import TopFooter from '@/components/TopFooter.vue';

export default {
    name: 'MainFooter',

    components: {
        TopFooter
    }
}
</script>

<style scoped lang="scss">
footer {
    background-image: url('../assets/img/footer-bg.jpg');
    background-position: center;
    background-size: cover;
    
    .centerFooter {
        padding: 50PX 0;
        display: flex;
        gap: 30px;
        position: relative;
        overflow: hidden;
        
        .logo-footer{
            position: absolute;
            top: -120px;
            right: 0;
            width: 650px;
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

                &:hover {
                    color: #fff;
                }
            }
        }
    }

    .bottom {
        background-color: #303030;
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