<script>
import FooterLinks from './FooterLinks.vue';

export default {
    data() {
        return {};
    },
    components: {
        FooterLinks
    }
};
</script>

<template>
    <div class="upperFooter d-flex">
        <FooterLinks/>
        <img src="../../public/img/dc-logo-bg.png" alt="">
    </div>
    <div class="sign-up d-flex justify-content-between">
        <div class="sign-up-button">
            <button>SIGN-UP NOW!</button>
        </div>
        <div class="follow-us d-flex align-items-center">
            <div class="follow-us-text">FOLLOW US</div>
            <div class="social-icons d-flex">
                
                <img src="../../public/img/footer-facebook.png" alt="Facebook">
                <img src="../../public/img/footer-twitter.png" alt="Twitter">
                <img src="../../public/img/footer-youtube.png" alt="YouTube">
                <img src="../../public/img/footer-pinterest.png" alt="Pinterest">
                
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>

@use '../styles/partials/variables' as *;


.upperFooter {
    height: 400px;
    background-image: url(../../public/img/footer-bg.jpg);
    position: relative;
    overflow: hidden;

    img {
       height: 120%;
       position: absolute;
       left: 70%;
       top: -3rem;
       bottom: 0;
    }
}

.sign-up {
    background-color: #303030;
    padding: 1rem 10rem;

    .sign-up-button {
        button {
            background-color: transparent;
            color: white;
            border: 3px solid $dc-blue;
            padding: 0.5rem 1rem;
            cursor: pointer;
            font-weight: bold;
        }
    }

    .follow-us {
        display: flex;
        align-items: center;

        .follow-us-text {
            color: $dc-blue;
            margin-right: 1rem;
            font-weight: bold;
            cursor: pointer;
        }

        .social-icons {
            display: flex;

            img {
                width: 24px;
                height: 24px;
                margin-left: 0.5rem;
                cursor: pointer;
            }
        }
    }
}
</style>

