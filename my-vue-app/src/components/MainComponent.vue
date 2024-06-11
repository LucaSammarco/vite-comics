<script>

import ListProducts from './ListProducts.vue';
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

    components: {
        ListProducts
    },

    props: {
        messaggio: String,
    },
    
};
</script>



<template>
    <main class="d-flex flex-column">

        <div class="jumbothrone h-50">
            <img src="../../public/img/jumbotron.jpg" alt="jumbothrone" >
            <div>
             <p class="series">current series</p>
            </div>


        </div>

        <ListProducts/>

        <div class="button-container">

            <button type="button" class="bottone btn ">Load More</button>

        </div>


        <div class="images-container d-flex justify-content-center">
            <div class="images  main-content">

                <ul class="d-flex p-0 m-0 justify-content-between p-3">
                    <li v-for="item in items" :key="item.id" class="image-item d-flex align-items-center list-unstyled me-5 mb-3 p-">

                        <img :src="item.url" :alt="item.text" class="me-3">
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

.jumbothrone {

    position: relative;

    img {
        height: 300px;
        width: 100%;
        object-fit: cover;
        object-position: top;

    }

    .series {
        background-color: $dc-blue;
        position: absolute;
        left: 10rem;
        bottom: -2rem;
        text-transform: uppercase;
        color: white;
        padding: 0.2rem 1.5rem;
        font-weight: bold;
        font-size: 1.1rem;
    }


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


.button-container{
    display: flex;
    justify-content: center;
    background-color: #1c1c1c;
    padding-bottom: 2rem;
    
    .bottone {
        padding: 0.2rem 4rem;
        margin-bottom: 0.5rem;
        font-family: 'Roboto' sans-serif !important ;
        text-transform: uppercase;
        font-weight: bold;
        border-radius: 0;
        background-color: $dc-blue;
        color: white;
    }
}



</style>