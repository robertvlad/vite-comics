<script>
  export default {
    data() {
        return {
            menuItems: [
                {
                    label: "Characters",
                    url: "#",
                    active: false
                },
                {
                    label: "Comics",
                    url: "#",
                    active: true
                },
                {
                    label: "Movies",
                    url: "#",
                    active: false
                },
                {
                    label: "Tv",
                    url: "#",
                    active: false
                },
                {
                    label: "Games",
                    url: "#",
                    active: false
                },
                {
                    label: "Collectibles",
                    url: "#",
                    active: false
                },
                {
                    label: "Videos",
                    url: "#",
                    active: false
                },
                {
                    label: "Fans",
                    url: "#",
                    active: false
                },
                {
                    label: "News",
                    url: "#",
                    active: false
                },
                {
                    label: "Shop",
                    url: "#",
                    active: false
                },
            ]
        }
    },
  }
</script>


<template lang="">
    <header class="container">
        <div class="navbar">
            <div class="logo">
                <a href="#">
                    <img src="../../public/img/dc-logo.png" alt="DC">
                </a>
            </div>
            <nav>
                <ul>
                    <li v-for="(item, index) in menuItems" ::key="index" :class="item.active ? 'active' : ''">
                        <a :href="item.url" :class="item.active ? 'active' : ''" >
                            {{ item.label }}
                        </a>                        
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>


<style lang="scss">
    @use "../styles/partials/variables" as *;

    .navbar{
        display: flex;
        justify-content: space-between;
        margin: 1rem 0;
        align-items: center;

        ul{
            list-style: none;
            display: flex;
            
            li{
                padding: 10px;

                &.active{
                border-bottom: $border-btn-blue
                }

                a.active{
                    color: $blue-color;
                }
            } 
            
            li:hover{
                border-bottom: $border-btn-blue
            }
            
            a{
                &:hover{
                    color: $blue-color;
                }
            }
        }
    }
</style>