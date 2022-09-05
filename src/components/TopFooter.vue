<template>
    <div class="top">
        <div class="container">
            <nav class="navbar p-5">
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/buy-comics-digital-comics.png" width="50" height="60"
                        class="d-inline-block align-top" alt="">
                    DIGITAL COMICS
                </a>
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/buy-comics-merchandise.png" width="60" height="60"
                        class="d-inline-block align-top" alt="">
                    DC MERCHANDISE
                </a>
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/buy-comics-subscriptions.png" width="60" height="60"
                        class="d-inline-block align-top" alt="">
                    SUBSCRIPTION
                </a>
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/buy-comics-shop-locator.png" width="40" height="60"
                        class="d-inline-block align-top" alt="">
                    COMIC SHOP LOACATOR
                </a>
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/buy-dc-power-visa.svg" width="60" height="60" class="d-inline-block align-top"
                        alt="">
                    DC POWER VISA
                </a>
            </nav>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TopFooter'
}
</script>

<style lang="scss">
.top {
    background-color: #0282f9;

    a {
        color: #fff;
        font-size: 1rem;
        display: flex;
        align-items: center;
        gap: 10px;

        &:hover {
            color: #fff;
        }
    }
}
</style>