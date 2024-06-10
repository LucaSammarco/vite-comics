<script>
export default {
    data() {
        return {
            items: [
                {
                    id: 1,
                    text: 'DIGITAL COMICS',
                    url: '/img/buy-comics-digital-comics.png'
                },
                {
                    id: 2,
                    text: 'DC MERCHANDISE',
                    url: '/img/buy-comics-merchandise.png'
                },
                {
                    id: 3,
                    text: 'SUBSCRIPTION',
                    url: '/img/buy-comics-subscriptions.png'
                },
                {
                    id: 4,
                    text: 'COMIC SHOP LOCATOR',
                    url: '/img/buy-comics-shop-locator.png'
                },
                {
                    id: 5,
                    text: 'DC POWER VISA',
                    url: '/img/buy-dc-power-visa.svg'
                }
            ]
        };
    },
    
};
</script>



<template>
    <main class="d-flex flex-column">

        <div class="main-content bg-dark text-white">
            <h2 class="ps-">--> Content goes here <--</h2>
        </div>

        <div class="images-container d-flex justify-content-center">
            <div class="images align-items-center main-content">

                <ul class="d-flex p-0 m-0  align-items-center ">
                    <li v-for="item in items" :key="item.id" class="image-item d-flex align-items-center list-unstyled me-5 mb-2">
                        <img :src="item.url" :alt="item.text" class="me-2">
                        <span><p>{{ item.text }}</p></span>
                    </li>
                </ul>
            </div>
        </div>
    </main>
</template>




<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.main-content {

    padding: 2rem 10rem;
}

.images-container{
    background-color: $dc-blue;
}


.images {
    
 

    ul {
        display: flex;
        padding: 1rem;
        
        margin: 0;
    }

    li {
        display: flex;
        align-items: center;
        list-style: none;
    }

    img {
        max-width: 50px;
        height: auto;
       
        margin-right: 10px;
    }

    span {
        display: flex;
        align-items: center;
    }

    p {
        margin-top: 0;
        margin-bottom: 0;
        color: white;
        white-space: nowrap;
    }
}

</style>