<script>
    export default {
        data(){
            return {

                headerLinks: [
                { title: 'Characters', id: 1, active: false },
                { title: 'Comics', id: 2, active: false },
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
            <img src="../assets/img/dc-logo.png" alt="">
        </section>

        <section class="navbar">
            
                <nav>
                    <ul>
                     
                        <li >
                            {{ headerLinks[0] }}
                        </li>

                    </ul>
                </nav>

        </section>

    </header>

</template>



<style lang="scss" scoped>

   @use '../styles/partials/variables' as *;

   li.active{
    background-color: $active-link-bg;
   }
    
</style>