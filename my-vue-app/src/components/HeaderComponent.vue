<script>
    export default {
        data(){
            return {

                headerLinks: [
                { title: 'Characters', id: 1, active: false },
                { title: 'Comics', id: 2, active: true },
                { title: 'Movies', id: 3, active: false },
                { title: 'TV', id: 4, active: false },
                { title: 'Games', id: 5, active: false },
                { title: 'Collectibles', id: 6, active: false },
                { title: 'Videos', id: 7, active: false },
                { title: 'Fans', id: 8, active: false },
                { title: 'News', id: 9, active: false },
                { title: 'Shop', id: 10, active: false }
            ]
            }
        }
    }

</script>

<template>

 

    <header class="d-flex">
       
        <section class="logo">
            <img src="/img/dc-logo.png" alt="DC Logo">
        </section>

        <section class="navbar ms-auto">
            
                <nav>
                    <ul class="d-flex ">
                     
                        <li v-for="link in headerLinks" :key="link.id"  :class="(link.active) ? 'active' : '' "  class="me-4 text-uppercase fw-bold" >
                            {{ link.title }}
                        </li>

                    </ul>
                </nav>

        </section>

    </header>

</template>



<style lang="scss" scoped>

   @use '../styles/partials/variables' as *;

   li {
    list-style: none;
   
}

li.active {
    color: $active-link-bg;
    position: relative; 
 
    &::after {
        content: '';
        position: absolute;
        bottom: -150%; 
        left: 0;
        width: 100%;
        border-bottom: 7px solid $active-link-bg;
    }
}



    
    
</style>