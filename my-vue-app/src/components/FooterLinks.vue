<script>
export default {
    data(){
        return {
            linkSections: [
                {
                    links: [
                        { title: 'DC COMICS', id: 0, isTitle: true },
                        { title: 'Characters', id: 1, active: false },
                        { title: 'Comics', id: 2, active: false },
                        { title: 'Movies', id: 3, active: false },
                        { title: 'TV', id: 4, active: false },
                        { title: 'Games', id: 5, active: false },
                        { title: 'Videos', id: 6, active: false },
                        { title: 'News', id: 7, active: false }
                    ]
                },
                {
                    links: [
                        { title: 'DC', id: 0, isTitle: true },
                        { title: 'Terms Of Use', id: 8, active: false },
                        { title: 'Privacy policy (New)', id: 9, active: false },
                        { title: 'Ad Choices', id: 10, active: false },
                        { title: 'Advertising', id: 11, active: false },
                        { title: 'Jobs', id: 12, active: false },
                        { title: 'Subscriptions', id: 13, active: false },
                        { title: 'Talent Workshops', id: 14, active: false },
                        { title: 'CPSC Certificates', id: 15, active: false },
                        { title: 'Ratings', id: 16, active: false },
                        { title: 'Shop Help', id: 17, active: false },
                        { title: 'Contact Us', id: 18, active: false }
                    ]
                },
                {
                    links: [
                        { title: 'SITES', id: 0, isTitle: true },
                        { title: 'DC', id: 19, active: false },
                        { title: 'MAD Magazine', id: 20, active: false },
                        { title: 'DC Kids', id: 21, active: false },
                        { title: 'DC Universe', id: 22, active: false },
                        { title: 'DC Power Visa', id: 23, active: false }
                    ]
                },
                {
                    links: [
                        { title: 'SHOP', id: 0, isTitle: true },
                        { title: 'Shop DC', id: 24, active: false },
                        { title: 'Shop DC Collectibles', id: 25, active: false }
                    ]
                }
            ]
        }
    }
}
</script>

<template>
    <div class="links d-flex">



        <div class="ComicsShop">
            <ul>
                <li v-for="link in linkSections[0].links" :key="link.id" :class="link.isTitle ? 'title' : ''">
                    {{ link.title }}
                </li>
            </ul>
            <ul>
                <li v-for="link in linkSections[3].links" :key="link.id" :class="link.isTitle ? 'title' : ''">
                    {{ link.title }}
                </li>
            </ul>
        </div>

        <div class="ComicsShop">
            <ul>
                <li v-for="link in linkSections[1].links" :key="link.id" :class="link.isTitle ? 'title' : ''">
                    {{ link.title }}
                </li>
            </ul>
          
        </div>

        <div class="ComicsShop">
            <ul>
                <li v-for="link in linkSections[2].links" :key="link.id" :class="link.isTitle ? 'title' : ''">
                    {{ link.title }}
                </li>
            </ul>
          
        </div>

        

    </div>


   
</template>

<style lang="scss" scoped>
.links {
   
    padding: 3rem 10rem;
    li {
        color:#6e6f70;
        list-style: none;
    }

    .title {
        font-weight: bold;
        color: white;
    }
}
</style>
